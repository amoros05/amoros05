{
  "annotations": {
    "list": [
      {
        "builtIn": 1,
        "datasource": "-- Grafana --",
        "enable": true,
        "hide": true,
        "iconColor": "rgba(0, 211, 255, 1)",
        "name": "Annotations & Alerts",
        "target": {
          "limit": 100,
          "matchAny": false,
          "tags": [],
          "type": "dashboard"
        },
        "type": "dashboard"
      }
    ]
  },
  "editable": true,
  "gnetId": null,
  "graphTooltip": 0,
  "id": 2,
  "iteration": 1634853034654,
  "links": [],
  "panels": [
    {
      "collapsed": false,
      "datasource": null,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 0
      },
      "id": 25,
      "panels": [],
      "title": "Challenge Progress",
      "type": "row"
    },
    {
      "cacheTimeout": null,
      "datasource": "Prometheus",
      "description": "",
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "decimals": 0,
          "mappings": [
            {
              "options": {
                "match": "null",
                "result": {
                  "text": "N/A"
                }
              },
              "type": "special"
            }
          ],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "#C8F2C2",
                "value": null
              },
              {
                "color": "#56A64B",
                "value": 20
              },
              {
                "color": "#37872D",
                "value": 60
              }
            ]
          },
          "unit": "percent"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 5,
        "w": 6,
        "x": 0,
        "y": 1
      },
      "id": 2,
      "interval": null,
      "links": [],
      "maxDataPoints": 100,
      "options": {
        "colorMode": "value",
        "graphMode": "area",
        "justifyMode": "auto",
        "orientation": "horizontal",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "text": {},
        "textMode": "auto"
      },
      "pluginVersion": "8.1.5",
      "repeat": "difficulties",
      "repeatDirection": "h",
      "targets": [
        {
          "expr": "sum without (category)(juiceshop_challenges_solved{difficulty=\"$difficulties\"}) / sum without (category)(juiceshop_challenges_total{difficulty=\"$difficulties\"}) * 100",
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "Solved $difficulties Star Challenges",
      "type": "stat"
    },
    {
      "datasource": null,
      "description": "",
      "gridPos": {
        "h": 5,
        "w": 6,
        "x": 12,
        "y": 6
      },
      "id": 129,
      "options": {
        "content": "![](https://raw.githubusercontent.com/OWASP/owasp-swag/master/projects/juice-shop/wallpapers/JuiceShop_Wallpaper_900x300.jpg)",
        "mode": "markdown"
      },
      "pluginVersion": "8.1.5",
      "transparent": true,
      "type": "text"
    },
    {
      "cacheTimeout": null,
      "datasource": null,
      "description": "",
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [
            {
              "options": {
                "match": "null",
                "result": {
                  "text": "N/A"
                }
              },
              "type": "special"
            }
          ],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "#299c46",
                "value": null
              },
              {
                "color": "rgba(237, 129, 40, 0.89)",
                "value": 0.33
              },
              {
                "color": "#d44a3a",
                "value": 0.66
              }
            ]
          },
          "unit": "percentunit"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 5,
        "w": 4,
        "x": 18,
        "y": 6
      },
      "id": 112,
      "interval": null,
      "links": [],
      "maxDataPoints": 100,
      "options": {
        "colorMode": "value",
        "graphMode": "area",
        "justifyMode": "auto",
        "orientation": "horizontal",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "text": {},
        "textMode": "auto"
      },
      "pluginVersion": "8.1.5",
      "targets": [
        {
          "exemplar": true,
          "expr": "juiceshop_cheat_score",
          "instant": false,
          "interval": "1m",
          "intervalFactor": 1,
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "Cheat Score",
      "type": "stat"
    },
    {
      "datasource": null,
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "red",
                "value": null
              },
              {
                "color": "orange",
                "value": 0.5
              },
              {
                "color": "green",
                "value": 0.75
              }
            ]
          },
          "unit": "percentunit"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 8,
        "w": 2,
        "x": 22,
        "y": 6
      },
      "id": 121,
      "options": {
        "colorMode": "value",
        "graphMode": "area",
        "justifyMode": "auto",
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "text": {},
        "textMode": "auto"
      },
      "pluginVersion": "8.1.5",
      "targets": [
        {
          "exemplar": true,
          "expr": "juiceshop_coding_challenges_accuracy{phase=\"find it\"}",
          "interval": "",
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "title": "\"Find It\" Accuracy",
      "type": "stat"
    },
    {
      "datasource": null,
      "fieldConfig": {
        "defaults": {
          "displayName": "",
          "mappings": [],
          "max": 100,
          "min": 1,
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "super-light-green",
                "value": null
              },
              {
                "color": "semi-dark-green",
                "value": 20
              },
              {
                "color": "dark-green",
                "value": 60
              }
            ]
          },
          "unit": "percent"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 11,
        "w": 18,
        "x": 0,
        "y": 11
      },
      "id": 78,
      "maxPerRow": 4,
      "options": {
        "colorMode": "value",
        "graphMode": "area",
        "justifyMode": "center",
        "orientation": "vertical",
        "reduceOptions": {
          "calcs": [
            "mean"
          ],
          "fields": "",
          "values": false
        },
        "text": {},
        "textMode": "auto"
      },
      "pluginVersion": "8.1.5",
      "repeat": null,
      "repeatDirection": "h",
      "targets": [
        {
          "exemplar": true,
          "expr": "sum by (category)(juiceshop_challenges_solved{}) / sum by (category)(juiceshop_challenges_total{}) * 100 != 0",
          "instant": false,
          "interval": "",
          "legendFormat": "{{category}}",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "Solved Challenges by Category",
      "type": "stat"
    },
    {
      "datasource": null,
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "palette-classic"
          },
          "custom": {
            "hideFrom": {
              "legend": false,
              "tooltip": false,
              "viz": false
            }
          },
          "mappings": []
        },
        "overrides": [
          {
            "matcher": {
              "id": "byName",
              "options": "unsolved"
            },
            "properties": [
              {
                "id": "color",
                "value": {
                  "fixedColor": "super-light-green",
                  "mode": "fixed"
                }
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "find it"
            },
            "properties": [
              {
                "id": "color",
                "value": {
                  "fixedColor": "green",
                  "mode": "fixed"
                }
              }
            ]
          },
          {
            "matcher": {
              "id": "byName",
              "options": "fix it"
            },
            "properties": [
              {
                "id": "color",
                "value": {
                  "fixedColor": "dark-green",
                  "mode": "fixed"
                }
              }
            ]
          }
        ]
      },
      "gridPos": {
        "h": 11,
        "w": 4,
        "x": 18,
        "y": 11
      },
      "id": 119,
      "options": {
        "displayLabels": [
          "value",
          "name"
        ],
        "legend": {
          "displayMode": "list",
          "placement": "bottom",
          "values": [
            "percent"
          ]
        },
        "pieType": "donut",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "tooltip": {
          "mode": "single"
        }
      },
      "pluginVersion": "8.1.5",
      "targets": [
        {
          "exemplar": true,
          "expr": "juiceshop_coding_challenges_progress",
          "interval": "",
          "legendFormat": "{{phase}}",
          "refId": "A"
        }
      ],
      "title": "Coding Challenge Progress",
      "type": "piechart"
    },
    {
      "datasource": null,
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "red",
                "value": null
              },
              {
                "color": "orange",
                "value": 0.5
              },
              {
                "color": "green",
                "value": 0.75
              }
            ]
          },
          "unit": "percentunit"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 8,
        "w": 2,
        "x": 22,
        "y": 14
      },
      "id": 122,
      "options": {
        "colorMode": "value",
        "graphMode": "area",
        "justifyMode": "auto",
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "text": {},
        "textMode": "auto"
      },
      "pluginVersion": "8.1.5",
      "targets": [
        {
          "exemplar": true,
          "expr": "juiceshop_coding_challenges_accuracy{phase=\"fix it\"}",
          "interval": "",
          "legendFormat": "",
          "refId": "A"
        }
      ],
      "title": "\"Fix It\" Accuracy",
      "type": "stat"
    },
    {
      "collapsed": true,
      "datasource": null,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 22
      },
      "id": 32,
      "panels": [
        {
          "aliasColors": {},
          "bars": false,
          "dashLength": 10,
          "dashes": false,
          "datasource": null,
          "fieldConfig": {
            "defaults": {
              "links": []
            },
            "overrides": []
          },
          "fill": 1,
          "fillGradient": 0,
          "gridPos": {
            "h": 5,
            "w": 24,
            "x": 0,
            "y": 16
          },
          "hiddenSeries": false,
          "id": 11,
          "legend": {
            "avg": false,
            "current": true,
            "max": false,
            "min": false,
            "show": true,
            "total": false,
            "values": true
          },
          "lines": true,
          "linewidth": 1,
          "nullPointMode": "null",
          "options": {
            "alertThreshold": true
          },
          "percentage": false,
          "pluginVersion": "8.1.5",
          "pointradius": 2,
          "points": false,
          "renderer": "flot",
          "seriesOverrides": [],
          "spaceLength": 10,
          "stack": false,
          "steppedLine": false,
          "targets": [
            {
              "expr": "juiceshop_user_social_interactions{}",
              "interval": "1m",
              "legendFormat": "{{type}}",
              "refId": "A"
            }
          ],
          "thresholds": [],
          "timeFrom": null,
          "timeRegions": [],
          "timeShift": null,
          "title": "Social Interactions",
          "tooltip": {
            "shared": true,
            "sort": 0,
            "value_type": "individual"
          },
          "type": "graph",
          "xaxis": {
            "buckets": null,
            "mode": "time",
            "name": null,
            "show": true,
            "values": []
          },
          "yaxes": [
            {
              "decimals": 0,
              "format": "short",
              "label": "",
              "logBase": 1,
              "max": null,
              "min": "0",
              "show": true
            },
            {
              "format": "short",
              "label": "",
              "logBase": 1,
              "max": null,
              "min": null,
              "show": true
            }
          ],
          "yaxis": {
            "align": false,
            "alignLevel": null
          }
        },
        {
          "aliasColors": {},
          "bars": true,
          "dashLength": 10,
          "dashes": false,
          "datasource": null,
          "fieldConfig": {
            "defaults": {
              "links": []
            },
            "overrides": []
          },
          "fill": 1,
          "fillGradient": 0,
          "gridPos": {
            "h": 6,
            "w": 9,
            "x": 0,
            "y": 21
          },
          "hiddenSeries": false,
          "id": 64,
          "legend": {
            "avg": false,
            "current": false,
            "max": false,
            "min": false,
            "show": true,
            "total": false,
            "values": false
          },
          "lines": false,
          "linewidth": 1,
          "nullPointMode": "null",
          "options": {
            "alertThreshold": true
          },
          "percentage": false,
          "pluginVersion": "8.1.5",
          "pointradius": 2,
          "points": false,
          "renderer": "flot",
          "seriesOverrides": [],
          "spaceLength": 10,
          "stack": false,
          "steppedLine": false,
          "targets": [
            {
              "expr": "increase(juiceshop_users_registered{}[1m])",
              "legendFormat": "{{type}}",
              "refId": "A"
            }
          ],
          "thresholds": [],
          "timeFrom": null,
          "timeRegions": [],
          "timeShift": null,
          "title": "User Signups",
          "tooltip": {
            "shared": true,
            "sort": 0,
            "value_type": "individual"
          },
          "type": "graph",
          "xaxis": {
            "buckets": null,
            "mode": "time",
            "name": null,
            "show": true,
            "values": []
          },
          "yaxes": [
            {
              "decimals": 0,
              "format": "short",
              "label": "",
              "logBase": 1,
              "max": null,
              "min": "0",
              "show": true
            },
            {
              "format": "short",
              "label": null,
              "logBase": 1,
              "max": null,
              "min": null,
              "show": true
            }
          ],
          "yaxis": {
            "align": false,
            "alignLevel": null
          }
        },
        {
          "cacheTimeout": null,
          "datasource": null,
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "mappings": [
                {
                  "options": {
                    "match": "null",
                    "result": {
                      "text": "N/A"
                    }
                  },
                  "type": "special"
                }
              ],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "#d44a3a",
                    "value": null
                  },
                  {
                    "color": "rgba(237, 129, 40, 0.89)",
                    "value": 10
                  },
                  {
                    "color": "#299c46",
                    "value": 25
                  }
                ]
              },
              "unit": "Orders placed"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 4,
            "x": 9,
            "y": 21
          },
          "id": 97,
          "interval": null,
          "links": [],
          "maxDataPoints": 100,
          "options": {
            "colorMode": "value",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "horizontal",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "text": {},
            "textMode": "auto"
          },
          "pluginVersion": "8.1.5",
          "targets": [
            {
              "expr": "juiceshop_orders_placed_total",
              "instant": false,
              "interval": "1m",
              "intervalFactor": 1,
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "timeFrom": null,
          "timeShift": null,
          "title": "Conversion Rate",
          "type": "stat"
        },
        {
          "cacheTimeout": null,
          "datasource": null,
          "fieldConfig": {
            "defaults": {
              "color": {
                "mode": "thresholds"
              },
              "decimals": 2,
              "mappings": [
                {
                  "options": {
                    "match": "null",
                    "result": {
                      "text": "N/A"
                    }
                  },
                  "type": "special"
                }
              ],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "#d44a3a",
                    "value": null
                  },
                  {
                    "color": "rgba(237, 129, 40, 0.89)",
                    "value": 100
                  },
                  {
                    "color": "#299c46",
                    "value": 5000
                  }
                ]
              },
              "unit": "¤"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 6,
            "w": 5,
            "x": 13,
            "y": 21
          },
          "id": 98,
          "interval": null,
          "links": [],
          "maxDataPoints": 100,
          "options": {
            "colorMode": "value",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "horizontal",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "text": {},
            "textMode": "auto"
          },
          "pluginVersion": "8.1.5",
          "targets": [
            {
              "expr": "juiceshop_wallet_balance_total",
              "instant": false,
              "interval": "1m",
              "intervalFactor": 1,
              "legendFormat": "",
              "refId": "A"
            }
          ],
          "timeFrom": null,
          "timeShift": null,
          "title": "Digital Wallets Total",
          "type": "stat"
        },
        {
          "cacheTimeout": null,
          "datasource": null,
          "fieldConfig": {
            "defaults": {
              "color": {
                "fixedColor": "rgb(31, 120, 193)",
                "mode": "fixed"
              },
              "decimals": 0,
              "mappings": [
                {
                  "options": {
                    "match": "null",
                    "result": {
                      "text": "N/A"
                    }
                  },
                  "type": "special"
                }
              ],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green",
                    "value": null
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "Standard Users"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 3,
            "w": 6,
            "x": 18,
            "y": 21
          },
          "id": 13,
          "interval": null,
          "links": [],
          "maxDataPoints": 100,
          "options": {
            "colorMode": "none",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "horizontal",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "text": {},
            "textMode": "auto"
          },
          "pluginVersion": "8.1.5",
          "targets": [
            {
              "expr": "juiceshop_users_registered{type=\"standard\"}",
              "refId": "A"
            }
          ],
          "timeFrom": null,
          "timeShift": null,
          "title": "Customer Base",
          "type": "stat"
        },
        {
          "cacheTimeout": null,
          "datasource": null,
          "fieldConfig": {
            "defaults": {
              "color": {
                "fixedColor": "rgb(31, 120, 193)",
                "mode": "fixed"
              },
              "decimals": 0,
              "mappings": [
                {
                  "options": {
                    "match": "null",
                    "result": {
                      "text": "N/A"
                    }
                  },
                  "type": "special"
                }
              ],
              "thresholds": {
                "mode": "absolute",
                "steps": [
                  {
                    "color": "green",
                    "value": null
                  },
                  {
                    "color": "red",
                    "value": 80
                  }
                ]
              },
              "unit": "Deluxe Users"
            },
            "overrides": []
          },
          "gridPos": {
            "h": 3,
            "w": 6,
            "x": 18,
            "y": 24
          },
          "id": 14,
          "interval": null,
          "links": [],
          "maxDataPoints": 100,
          "options": {
            "colorMode": "none",
            "graphMode": "area",
            "justifyMode": "auto",
            "orientation": "horizontal",
            "reduceOptions": {
              "calcs": [
                "lastNotNull"
              ],
              "fields": "",
              "values": false
            },
            "text": {},
            "textMode": "auto"
          },
          "pluginVersion": "8.1.5",
          "targets": [
            {
              "expr": "juiceshop_users_registered{type=\"deluxe\"}",
              "refId": "A"
            }
          ],
          "timeFrom": null,
          "timeShift": null,
          "title": " ",
          "type": "stat"
        }
      ],
      "title": "Business Metrics",
      "type": "row"
    },
    {
      "collapsed": false,
      "datasource": null,
      "gridPos": {
        "h": 1,
        "w": 24,
        "x": 0,
        "y": 23
      },
      "id": 39,
      "panels": [],
      "title": "Technical",
      "type": "row"
    },
    {
      "aliasColors": {},
      "bars": true,
      "dashLength": 10,
      "dashes": false,
      "datasource": null,
      "fieldConfig": {
        "defaults": {
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 6,
        "w": 24,
        "x": 0,
        "y": 24
      },
      "hiddenSeries": false,
      "id": 71,
      "legend": {
        "avg": false,
        "current": false,
        "max": false,
        "min": false,
        "show": true,
        "total": false,
        "values": false
      },
      "lines": false,
      "linewidth": 1,
      "nullPointMode": "null",
      "options": {
        "alertThreshold": true
      },
      "percentage": false,
      "pluginVersion": "8.1.5",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [
        {
          "alias": "2XX",
          "color": "#37872D"
        },
        {
          "alias": "3XX",
          "color": "#96D98D"
        },
        {
          "alias": "4XX",
          "color": "#FF780A"
        },
        {
          "alias": "5XX",
          "color": "#C4162A"
        }
      ],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "increase(http_requests_count{app=\"juiceshop\"}[1m])",
          "interval": "1m",
          "legendFormat": "{{status_code}}",
          "refId": "A"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "HTTP Requests",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": "Requests per Minute",
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "cacheTimeout": null,
      "datasource": null,
      "fieldConfig": {
        "defaults": {
          "displayName": "",
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "none"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 5,
        "w": 9,
        "x": 0,
        "y": 30
      },
      "id": 90,
      "links": [],
      "options": {
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "mean"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true,
        "text": {}
      },
      "pluginVersion": "8.1.5",
      "targets": [
        {
          "expr": "rate(file_uploads_count[1h]) * 3600",
          "instant": false,
          "interval": "1m",
          "intervalFactor": 1,
          "legendFormat": "{{file_type}}",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "File Uploads",
      "type": "gauge"
    },
    {
      "cacheTimeout": null,
      "datasource": null,
      "fieldConfig": {
        "defaults": {
          "displayName": "",
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "short"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 5,
        "w": 15,
        "x": 9,
        "y": 30
      },
      "id": 91,
      "links": [],
      "options": {
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "mean"
          ],
          "fields": "",
          "values": false
        },
        "showThresholdLabels": false,
        "showThresholdMarkers": true,
        "text": {}
      },
      "pluginVersion": "8.1.5",
      "targets": [
        {
          "expr": "rate(file_upload_errors[1h]) * 3600",
          "interval": "1m",
          "intervalFactor": 1,
          "legendFormat": "{{file_type}}",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "File Upload Errors",
      "type": "gauge"
    },
    {
      "datasource": null,
      "fieldConfig": {
        "defaults": {
          "mappings": [],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "s"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 6,
        "w": 24,
        "x": 0,
        "y": 35
      },
      "id": 105,
      "options": {
        "displayMode": "gradient",
        "orientation": "auto",
        "reduceOptions": {
          "calcs": [
            "mean"
          ],
          "fields": "",
          "values": false
        },
        "showUnfilled": true,
        "text": {}
      },
      "pluginVersion": "8.1.5",
      "targets": [
        {
          "expr": "sort_desc(avg by (task)(juiceshop_startup_duration_seconds))",
          "format": "time_series",
          "instant": true,
          "interval": "",
          "legendFormat": "{{ task }}",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "Startup Duration",
      "type": "bargauge"
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 10,
        "w": 9,
        "x": 0,
        "y": 41
      },
      "hiddenSeries": false,
      "id": 46,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "options": {
        "alertThreshold": true
      },
      "paceLength": 10,
      "percentage": false,
      "pluginVersion": "8.1.5",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "irate(process_cpu_user_seconds_total{}[2m]) * 100",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "User CPU",
          "refId": "A"
        },
        {
          "expr": "irate(process_cpu_system_seconds_total{}[2m]) * 100",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Sys CPU",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Process CPU Usage",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "percent",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 10,
        "w": 7,
        "x": 9,
        "y": 41
      },
      "hiddenSeries": false,
      "id": 48,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "options": {
        "alertThreshold": true
      },
      "paceLength": 10,
      "percentage": false,
      "pluginVersion": "8.1.5",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "nodejs_eventloop_lag_seconds{}",
          "format": "time_series",
          "intervalFactor": 1,
          "refId": "A"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Event Loop Lag",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "s",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "cacheTimeout": null,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "color": {
            "fixedColor": "#F2495C",
            "mode": "fixed"
          },
          "mappings": [
            {
              "options": {
                "match": "null",
                "result": {
                  "text": "N/A"
                }
              },
              "type": "special"
            }
          ],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "none"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 6,
        "w": 5,
        "x": 16,
        "y": 41
      },
      "id": 52,
      "interval": null,
      "links": [],
      "maxDataPoints": 100,
      "options": {
        "colorMode": "none",
        "graphMode": "area",
        "justifyMode": "auto",
        "orientation": "horizontal",
        "reduceOptions": {
          "calcs": [
            "lastNotNull"
          ],
          "fields": "",
          "values": false
        },
        "text": {},
        "textMode": "auto"
      },
      "pluginVersion": "8.1.5",
      "targets": [
        {
          "exemplar": true,
          "expr": "sum(changes(process_start_time_seconds{}[$__rate_interval]))",
          "format": "time_series",
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "{{instance}}",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "Number of Process Restarts",
      "type": "stat"
    },
    {
      "cacheTimeout": null,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [
            {
              "options": {
                "match": "null",
                "result": {
                  "text": "N/A"
                }
              },
              "type": "special"
            }
          ],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "none"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 3,
        "w": 3,
        "x": 21,
        "y": 41
      },
      "id": 84,
      "interval": "",
      "links": [],
      "maxDataPoints": 100,
      "options": {
        "colorMode": "none",
        "graphMode": "none",
        "justifyMode": "auto",
        "orientation": "horizontal",
        "reduceOptions": {
          "calcs": [
            "mean"
          ],
          "fields": "",
          "values": false
        },
        "text": {},
        "textMode": "name"
      },
      "pluginVersion": "8.1.5",
      "targets": [
        {
          "expr": "sum(juiceshop_version_info{}) by (version)",
          "format": "time_series",
          "instant": false,
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "{{version}}",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "Juice Shop Version",
      "type": "stat"
    },
    {
      "cacheTimeout": null,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "color": {
            "mode": "thresholds"
          },
          "mappings": [
            {
              "options": {
                "match": "null",
                "result": {
                  "text": "N/A"
                }
              },
              "type": "special"
            }
          ],
          "thresholds": {
            "mode": "absolute",
            "steps": [
              {
                "color": "green",
                "value": null
              },
              {
                "color": "red",
                "value": 80
              }
            ]
          },
          "unit": "none"
        },
        "overrides": []
      },
      "gridPos": {
        "h": 3,
        "w": 3,
        "x": 21,
        "y": 44
      },
      "id": 50,
      "interval": "",
      "links": [],
      "maxDataPoints": 100,
      "options": {
        "colorMode": "none",
        "graphMode": "none",
        "justifyMode": "auto",
        "orientation": "horizontal",
        "reduceOptions": {
          "calcs": [
            "mean"
          ],
          "fields": "",
          "values": false
        },
        "text": {},
        "textMode": "name"
      },
      "pluginVersion": "8.1.5",
      "targets": [
        {
          "expr": "sum(nodejs_version_info{}) by (version)",
          "format": "time_series",
          "instant": false,
          "interval": "",
          "intervalFactor": 1,
          "legendFormat": "{{version}}",
          "refId": "A"
        }
      ],
      "timeFrom": null,
      "timeShift": null,
      "title": "Node.js Version",
      "type": "stat"
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 11,
        "w": 8,
        "x": 16,
        "y": 47
      },
      "hiddenSeries": false,
      "id": 56,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "options": {
        "alertThreshold": true
      },
      "paceLength": 10,
      "percentage": false,
      "pluginVersion": "8.1.5",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "nodejs_active_handles_total{}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Active Handler",
          "refId": "A"
        },
        {
          "expr": "nodejs_active_requests_total{}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Active Request",
          "refId": "B"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Active Handlers/Requests Total",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    },
    {
      "aliasColors": {},
      "bars": false,
      "dashLength": 10,
      "dashes": false,
      "datasource": "Prometheus",
      "fieldConfig": {
        "defaults": {
          "links": []
        },
        "overrides": []
      },
      "fill": 1,
      "fillGradient": 0,
      "gridPos": {
        "h": 7,
        "w": 16,
        "x": 0,
        "y": 51
      },
      "hiddenSeries": false,
      "id": 54,
      "legend": {
        "alignAsTable": true,
        "avg": true,
        "current": true,
        "max": true,
        "min": true,
        "rightSide": true,
        "show": true,
        "total": false,
        "values": true
      },
      "lines": true,
      "linewidth": 1,
      "links": [],
      "nullPointMode": "null",
      "options": {
        "alertThreshold": true
      },
      "paceLength": 10,
      "percentage": false,
      "pluginVersion": "8.1.5",
      "pointradius": 2,
      "points": false,
      "renderer": "flot",
      "seriesOverrides": [],
      "spaceLength": 10,
      "stack": false,
      "steppedLine": false,
      "targets": [
        {
          "expr": "process_resident_memory_bytes{}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Process Memory",
          "refId": "A"
        },
        {
          "expr": "nodejs_heap_size_total_bytes{}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Heap Total",
          "refId": "B"
        },
        {
          "expr": "nodejs_heap_size_used_bytes{}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "Heap Used",
          "refId": "C"
        },
        {
          "expr": "nodejs_external_memory_bytes{}",
          "format": "time_series",
          "intervalFactor": 1,
          "legendFormat": "External Memory",
          "refId": "D"
        }
      ],
      "thresholds": [],
      "timeFrom": null,
      "timeRegions": [],
      "timeShift": null,
      "title": "Process Memory Usage",
      "tooltip": {
        "shared": true,
        "sort": 0,
        "value_type": "individual"
      },
      "type": "graph",
      "xaxis": {
        "buckets": null,
        "mode": "time",
        "name": null,
        "show": true,
        "values": []
      },
      "yaxes": [
        {
          "format": "bytes",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        },
        {
          "format": "short",
          "label": null,
          "logBase": 1,
          "max": null,
          "min": null,
          "show": true
        }
      ],
      "yaxis": {
        "align": false,
        "alignLevel": null
      }
    }
  ],
  "refresh": "10s",
  "schemaVersion": 30,
  "style": "dark",
  "tags": [],
  "templating": {
    "list": [
      {
        "allValue": null,
        "current": {
          "text": "1 + 2 + 3 + 4 + 5 + 6",
          "value": [
            "1",
            "2",
            "3",
            "4",
            "5",
            "6"
          ]
        },
        "description": null,
        "error": null,
        "hide": 2,
        "includeAll": true,
        "label": "Difficulty Levels supported by JuiceShop",
        "multi": true,
        "name": "difficulties",
        "options": [
          {
            "selected": false,
            "text": "All",
            "value": "$__all"
          },
          {
            "selected": true,
            "text": "1",
            "value": "1"
          },
          {
            "selected": true,
            "text": "2",
            "value": "2"
          },
          {
            "selected": true,
            "text": "3",
            "value": "3"
          },
          {
            "selected": true,
            "text": "4",
            "value": "4"
          },
          {
            "selected": true,
            "text": "5",
            "value": "5"
          },
          {
            "selected": true,
            "text": "6",
            "value": "6"
          }
        ],
        "query": "1,2,3,4,5,6",
        "skipUrlSync": false,
        "type": "custom"
      }
    ]
  },
  "time": {
    "from": "now-1h",
    "to": "now"
  },
  "timepicker": {
    "refresh_intervals": [
      "5s",
      "10s",
      "30s",
      "1m",
      "5m",
      "15m",
      "30m",
      "1h",
      "2h",
      "1d"
    ]
  },
  "timezone": "",
  "title": "Juice Shop Instance Status",
  "uid": "Sj-cIdwZk",
  "version": 18
}
