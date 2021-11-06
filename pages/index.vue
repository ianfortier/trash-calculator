<template>
  <v-container>
    <v-row justify="space-around">
      <v-col cols="auto" align="center">
        <v-card outlined width="500" color="grey lighten-3">
          <v-row no-gutters>
            <v-col cols="12">
              <v-sheet height="100" color="black">
                <div
                  class="
                    text-h2 text-right
                    white--text
                    font-weight-medium
                    py-6
                    px-3
                  "
                  style="height: 100%"
                >
                  <span v-if="numberInput">{{ thisistrash }}</span>
                  <span v-else>{{ total }}</span>
                </div>
              </v-sheet>
            </v-col>
            <v-col cols="12">
              <v-row no-gutters>
                <v-col cols="3">
                  <v-card
                    @click="setAction('addition')"
                    height="80"
                    color="grey lighten-2"
                    link
                    outlined
                    tile
                    style="border-color: black !important"
                  >
                    <v-container fill-height fluid>
                      <v-row align="center" justify="center">
                        <v-col align-self="center" class="pa-0">
                          <div
                            class="text-h2 font-weight-medium"
                            style="height: 100%"
                          >
                            +
                          </div>
                        </v-col>
                      </v-row>
                    </v-container>
                  </v-card>
                </v-col>
                <v-col cols="3">
                  <v-card
                    @click="setAction('substraction')"
                    height="80"
                    color="grey lighten-2"
                    link
                    outlined
                    tile
                    style="border-color: black !important"
                  >
                    <v-container fill-height fluid>
                      <v-row align="center" justify="center">
                        <v-col align-self="center" class="pa-0">
                          <div
                            class="text-h2 font-weight-medium"
                            style="height: 100%"
                          >
                            −
                          </div>
                        </v-col>
                      </v-row>
                    </v-container>
                  </v-card>
                </v-col>
                <v-col cols="3">
                  <v-card
                    @click="setAction('multiplication')"
                    height="80"
                    color="grey lighten-2"
                    link
                    outlined
                    tile
                    style="border-color: black !important"
                  >
                    <v-container fill-height fluid>
                      <v-row align="center" justify="center">
                        <v-col align-self="center" class="pa-0">
                          <div
                            class="text-h2 font-weight-medium"
                            style="height: 100%"
                          >
                            ×
                          </div>
                        </v-col>
                      </v-row>
                    </v-container>
                  </v-card>
                </v-col>
                <v-col cols="3">
                  <v-card
                    @click="setAction('division')"
                    height="80"
                    color="grey lighten-2"
                    link
                    outlined
                    tile
                    style="border-color: black !important"
                  >
                    <v-container fill-height fluid>
                      <v-row align="center" justify="center">
                        <v-col align-self="center" class="pa-0">
                          <div
                            class="text-h2 font-weight-medium"
                            style="height: 100%"
                          >
                            ÷
                          </div>
                        </v-col>
                      </v-row>
                    </v-container>
                  </v-card>
                </v-col>
              </v-row>
            </v-col>
            <v-col cols="12">
              <v-row no-gutters>
                <v-col cols="9">
                  <v-row no-gutters>
                    <v-col cols="4">
                      <v-card
                        @click="inputNumber(1)"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                1
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        @click="inputNumber(2)"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                2
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        @click="inputNumber(3)"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                3
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        @click="inputNumber(4)"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                4
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        @click="inputNumber(5)"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                5
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        @click="inputNumber(6)"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                6
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        @click="inputNumber(7)"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                7
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        @click="inputNumber(8)"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                8
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        @click="inputNumber(9)"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                9
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        @click="inputNumber(0)"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                0
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                .
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                    <v-col cols="4">
                      <v-card
                        @click="clear"
                        height="80"
                        color="white"
                        link
                        outlined
                        tile
                        style="border-color: black !important"
                      >
                        <v-container fill-height fluid>
                          <v-row align="center" justify="center">
                            <v-col align-self="center" class="pa-0">
                              <div
                                class="text-h2 font-weight-medium"
                                style="height: 100%"
                              >
                                C
                              </div>
                            </v-col>
                          </v-row>
                        </v-container>
                      </v-card>
                    </v-col>
                  </v-row>
                </v-col>
                <v-col cols="3" class="orange">
                  <v-card
                    @click="calculate()"
                    color="transparent"
                    height="100%"
                    link
                    outlined
                    tile
                  >
                    <v-container fill-height fluid>
                      <v-row align="center" justify="center">
                        <v-col align-self="center" class="pa-0">
                          <div
                            class="text-h2 font-weight-medium"
                            style="height: 100%"
                          >
                            =
                          </div>
                        </v-col>
                      </v-row>
                    </v-container>
                  </v-card>
                </v-col>
              </v-row>
            </v-col>
          </v-row>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data() {
    return {
      total: null,
      numberInput: "",
      action: null,
    };
  },
  methods: {
    setAction(action) {
      if (action == this.action) {
        return;
      }
      this.action = action;
      this.calculate();
    },
    inputNumber(number) {
      this.numberInput = this.numberInput + "" + number;
    },
    addition() {
      this.total = this.total += parseFloat(this.numberInput);
      this.numberInput = "";
    },
    substraction() {
      this.total = this.total -= parseFloat(this.numberInput);
      this.numberInput = "";
    },
    multiplication() {
      this.total = this.total * this.numberInput;
      this.numberInput = "";
    },
    division() {
      this.total = this.total / this.numberInput;
      this.numberInput = "";
    },
    calculate() {
      if (!this.numberInput) {
        this.total = parseFloat(this.numberInput);
        return;
      }

      if (this.action == "addition") {
        this.addition();
      } else if (this.action == "substraction") {
        this.substraction();
      } else if (this.action == "multiplication") {
        this.multiplication();
      } else if (this.action == "division") {
        this.division();
      }
      this.numberInput = "";
    },
    clear() {
      this.total = null;
      this.numberInput = "";
      this.action = null;
    },
  },
};
</script>
