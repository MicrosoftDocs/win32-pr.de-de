---
title: BC6H-Format
description: Das BC6H-Format ist ein Texturkomprimierungsformat, das zur Unterstützung von HDR-Farbräumen (High Dynamic Range) in Quelldaten entwickelt wurde.
ms.assetid: D6A1A729-5023-4A94-A8DB-5954D453E136
keywords:
- BC6H
- DXGI_FORMAT_BC6H
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27422e177e98ecdc53b4152ba0514866f5ad75216e9ef789145d1af882a645d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633820"
---
# <a name="bc6h-format"></a>BC6H-Format

Das BC6H-Format ist ein Texturkomprimierungsformat, das zur Unterstützung von HDR-Farbräumen (High Dynamic Range) in Quelldaten entwickelt wurde.

-   [Informationen zum BC6H/DXGI-FORMAT \_ \_ BC6H](/windows)
-   [BC6H-Implementierung](#bc6h-implementation)
-   [Decodieren des BC6H-Formats](#decoding-the-bc6h-format)
-   [BC6H Compressed Endpoint Format](#bc6h-compressed-endpoint-format)
-   [Signieren der Erweiterung für Endpunktwerte](#sign-extension-for-endpoint-values)
-   [Transformationsinversion für Endpunktwerte](#transform-inversion-for-endpoint-values)
-   [Unquantisierung von Farbendpunkten](#unquantization-of-color-endpoints)
-   [Zugehörige Themen](#related-topics)

## <a name="about-bc6hdxgi_format_bc6h"></a>Informationen zum BC6H/DXGI-FORMAT \_ \_ BC6H

Das BC6H-Format bietet hochwertige Komprimierung für Bilder, die drei HDR-Farbkanäle verwenden, mit einem 16-Bit-Wert für jeden Farbkanal des Werts (16:16:16). Es gibt keine Unterstützung für einen Alphakanal.

BC6H wird durch die folgenden DXGI \_ FORMAT-Enumerationswerte angegeben:

-   **DXGI \_ FORMATIEREN \_ SIE BC6H \_ TYPELESS**.
-   **DXGI \_ FORMAT \_ BC6H \_ UF16**. Dieses BC6H-Format verwendet kein Vorzeichenbit in den 16-Bit-Gleitkommafarbkanalwerten.
-   **DXGI \_ FORMAT \_ BC6H \_ SF16**. Dieses BC6H-Format verwendet ein Vorzeichenbit in den 16-Bit-Gleitkommafarbkanalwerten.

> [!Note]  
> Das 16-Bit-Gleitkommaformat für Farbkanäle wird häufig als "halb" Gleitkommaformat bezeichnet. Dieses Format hat das folgende Bitlayout:
>
> |  Format                     | Bitlayout                                                |
> |-----------------------|-------------------------------------------------|
> | UF16 (float ohne Vorzeichen) | 5 Exponentenbits + 11 Mantissebits              |
> | SF16 (signed float)   | 1 Vorzeichenbit + 5 Exponentenbits + 10 Mantissebits |
>
> 
>
>  

 

Das BC6H-Format kann für [Textur2D-Texturressourcen](/windows/desktop/direct3d10/d3d10-graphics-reference-resource-structures) (einschließlich Arrays), Texture3D oder TextureCube (einschließlich Arrays) verwendet werden. Ebenso gilt dieses Format für alle MIP-Kartenoberflächen, die diesen Ressourcen zugeordnet sind.

BC6H verwendet eine feste Blockgröße von 16 Bytes (128 Bits) und eine feste Kachelgröße von 4x4 Texels. Wie bei vorherigen BC-Formaten werden Texturbilder, die größer als die unterstützte Kachelgröße (4 x 4) sind, mithilfe mehrerer Blöcke komprimiert. Diese Adressierungsidentität gilt auch für dreidimensionale Bilder, MIP-Karten, Cubemaps und Texturarrays. Alle Bildkacheln müssen das gleiche Format haben.

Einige wichtige Hinweise zum BC6H-Format:

-   BC6H unterstützt die Gleitkommadenormalisierung, jedoch keine INF (unendlich) und NaN (keine Zahl). Die Ausnahme ist der signierte Modus von BC6H (DXGI \_ FORMAT \_ BC6H \_ SF16), der -INF (negative Unendlichkeit) unterstützt. Beachten Sie, dass diese Unterstützung für -INF lediglich ein Artefakt des Formats selbst ist und nicht speziell von Encodern für dieses Format unterstützt wird. Wenn Encoder auf INF-Eingabedaten (positiv oder negativ) oder NaN-Eingabedaten stoßen, sollten sie diese Daten im Allgemeinen in den maximal zulässigen Nicht-INF-Darstellungswert konvertieren und NaN vor der Komprimierung \\ 0 zuordnen.
-   BC6H unterstützt keinen Alphakanal.
-   Der BC6H-Decoder führt eine Dekomprimierung durch, bevor er Texturfilterung ausführt.
-   Die BC6H-Dekomprimierung muss bitgenau sein. Das heißt, die Hardware muss Ergebnisse zurückgeben, die mit dem in dieser Dokumentation beschriebenen Decoder identisch sind.

## <a name="bc6h-implementation"></a>BC6H-Implementierung

Ein BC6H-Block besteht aus Modusbits, komprimierten Endpunkten, komprimierten Indizes und einem optionalen Partitionsindex. Dieses Format gibt 14 verschiedene Modi an.

Eine Endpunktfarbe wird als RGB-Triplet gespeichert. BC6H definiert eine Palette von Farben in einer ungefähren Linie über eine Reihe von definierten Farbendpunkten. Außerdem kann eine Kachel je nach Modus in zwei Regionen unterteilt oder als einzelne Region behandelt werden, wobei eine Kachel mit zwei Regionen über einen separaten Satz von Farbendpunkten für jede Region verfügt. BC6H speichert einen Palettenindex pro Texel.

Im Fall von zwei Regionen gibt es 32 mögliche Partitionen.

## <a name="decoding-the-bc6h-format"></a>Decodieren des BC6H-Formats

Der folgende Pseudocode zeigt die Schritte zum Dekomprimieren des Pixels bei (x,y) unter 16 Byte BC6H-Block.

``` syntax
decompress_bc6h(x, y, block)
{
    mode = extract_mode(block);
    endpoints;
    index;
    
    if(mode.type == ONE)
    {
        endpoints = extract_compressed_endpoints(mode, block);
        index = extract_index_ONE(x, y, block);
    }
    else //mode.type == TWO
    {
        partition = extract_partition(block);
        region = get_region(partition, x, y);
        endpoints = extract_compressed_endpoints(mode, region, block);
        index = extract_index_TWO(x, y, partition, block);
    }
    
    unquantize(endpoints);
    color = interpolate(index, endpoints);
    finish_unquantize(color);
}
```

Die folgende Tabelle enthält die Bitanzahl und werte für jedes der 14 möglichen Formate für BC6H-Blöcke. 

| Mode | Partitionsindizes | Partition | Farbendpunkte                  | Modusbits      |
|------|-------------------|-----------|----------------------------------|----------------|
| 1    | 46 Bit           | 5 Bits    | 75 Bits (10,555, 10,555, 10,555) | 2 Bits (00)    |
| 2    | 46 Bit           | 5 Bits    | 75 Bits (7666, 7666, 7666)       | 2 Bits (01)    |
| 3    | 46 Bit           | 5 Bits    | 72 Bits (11,555, 11,444, 11,444) | 5 Bits (00010) |
| 4    | 46 Bit           | 5 Bits    | 72 Bits (11.444, 11.555, 11.444) | 5 Bits (00110) |
| 5    | 46 Bit           | 5 Bits    | 72 Bits (11.444, 11.444, 11.555) | 5 Bits (01010) |
| 6    | 46 Bit           | 5 Bits    | 72 Bits (9555, 9555, 9555)       | 5 Bits (01110) |
| 7    | 46 Bit           | 5 Bits    | 72 Bits (8666, 8555, 8555)       | 5 Bits (10010) |
| 8    | 46 Bit           | 5 Bits    | 72 Bits (8555, 8666, 8555)       | 5 Bits (10110) |
| 9    | 46 Bit           | 5 Bits    | 72 Bits (8555, 8555, 8666)       | 5 Bits (11010) |
| 10   | 46 Bit           | 5 Bits    | 72 Bits (6666, 6666, 6666)       | 5 Bits (11110) |
| 11   | 63 Bit           | 0 Bits    | 60 Bits (10,10, 10,10, 10,10)    | 5 Bits (00011) |
| 12   | 63 Bit           | 0 Bits    | 60 Bits (11,9, 11,9, 11,9)       | 5 Bits (00111) |
| 13   | 63 Bit           | 0 Bits    | 60 Bits (12,8, 12,8, 12,8)       | 5 Bits (01011) |
| 14   | 63 Bit           | 0 Bits    | 60 Bits (16,4, 16,4, 16,4)       | 5 Bits (01111) |



 

Jedes Format in dieser Tabelle kann durch die Modusbits eindeutig identifiziert werden. Die ersten zehn Modi werden für Kacheln mit zwei Bereichen verwendet, und das Modusbitfeld kann zwei oder fünf Bits lang sein. Diese Blöcke enthalten auch Felder für die komprimierten Farbendpunkte (72 oder 75 Bits), die Partition (5 Bits) und die Partitionsindizes (46 Bits).

Für die komprimierten Farbendpunkte notieren die Werte in der vorangehenden Tabelle die Genauigkeit der gespeicherten RGB-Endpunkte und die Anzahl der Bits, die für jeden Farbwert verwendet werden. Der Modus 3 gibt beispielsweise eine Genauigkeitsstufe des Farbendpunkts von 11 und die Anzahl der Bits an, die zum Speichern der Deltawerte der transformierten Endpunkte für die Rot-, Blau- und Grünfarben verwendet werden (5, 4 bzw. 4). Modus 10 verwendet keine Deltakomprimierung und speichert stattdessen alle vier Farbendpunkte explizit.

Die letzten vier Blockmodi werden für Kacheln mit einem Bereich verwendet, wobei das Modusfeld 5 Bits beträgt. Diese Blöcke enthalten Felder für die Endpunkte (60 Bits) und die komprimierten Indizes (63 Bits). Mode 11 (wie Mode 10) verwendet keine Deltakomprimierung und speichert stattdessen explizit beide Farbendpunkte.

Die Modi 10011, 10111, 11011 und 11111 (nicht angezeigt) sind reserviert. Verwenden Sie diese nicht in Ihrem Encoder. Wenn der Hardware Blöcke mit einem dieser Modi übergeben werden, muss der resultierende dekomprimierte Block alle Nullen in allen Kanälen mit Ausnahme des Alphakanals enthalten.

Für BC6H muss der Alphakanal unabhängig vom Modus immer 1.0 zurückgeben.

### <a name="bc6h-partition-set"></a>BC6H-Partitionssatz

Es gibt 32 mögliche Partitionssätze für eine Kachel mit zwei Regionen, die in der folgenden Tabelle definiert sind. Jeder 4x4-Block stellt eine einzelne Form dar.

![Tabelle mit bc6h-Partitionssätzen](images/bc6h-partition-sets.png)

In dieser Tabelle mit Partitionssätzen ist der fett formatierte und unterstrichene Eintrag der Speicherort des Fix up-Indexes für Teilmenge 1 (die mit einem Bit weniger angegeben wird). Der Fix up-Index für Teilmenge 0 ist immer Index 0, da die Partitionierung immer so angeordnet ist, dass Index 0 immer in Teilmenge 0 liegt. Die Partitions reihenfolge geht von oben links nach unten rechts, von links nach rechts und dann von oben nach unten.

## <a name="bc6h-compressed-endpoint-format"></a>BC6H Compressed Endpoint Format

![Bitfelder für bc6h-komprimierte Endpunktformate](images/bc6h-headers-med.png)

In dieser Tabelle werden die Bitfelder für die komprimierten Endpunkte als Funktion des Endpunktformats angezeigt. Jede Spalte gibt eine Codierung und jede Zeile ein Bitfeld an. Dieser Ansatz benötigt 82 Bits für Kacheln mit zwei Regionen und 65 Bits für Kacheln mit einem Bereich. Beispielsweise sind die ersten 5 Bits für die Codierung mit einem Bereich 16 4 oben (insbesondere die Spalte ganz rechts) die Bits m 4:0, die nächsten 10 Bits sind Bits rw 9:0 und so weiter mit den letzten 6 Bits, die bw \[ \] \[ \] \[ \] \[ 10:15 \] enthalten.

Die Feldnamen in der obigen Tabelle sind wie folgt definiert:

| Feld | Variable          |
|-------|-------------------|
| m     | Modus              |
| T     | Shape-Index       |
| Rw    | endpt \[ 0 \] . A \[ 0\] |
| Rx    | endpt \[ 0 \] . B \[ 0\] |
| Ry    | endpt \[ 1 \] . A \[ 0\] |
| Rz    | endpt \[ 1 \] . B \[ 0\] |
| Gw    | endpt \[ 0 \] . A \[ 1\] |
| Gx    | endpt \[ 0 \] . B \[ 1\] |
| Gy    | endpt \[ 1 \] . A \[ 1\] |
| gz    | endpt \[ 1 \] . B \[ 1\] |
| Bw    | endpt \[ 0 \] . A \[ 2\] |
| Bx    | endpt \[ 0 \] . B \[ 2\] |
| by    | endpt \[ 1 \] . A \[ 2\] |
| Bz    | endpt \[ 1 \] . B \[ 2\] |



 

Endpt i , wobei i entweder 0 oder 1 ist, bezieht sich auf den \[ \] 0. bzw. 1. Satz von Endpunkten.

## <a name="sign-extension-for-endpoint-values"></a>Signieren der Erweiterung für Endpunktwerte

Für Kacheln mit zwei Regionen gibt es vier Endpunktwerte, die erweitert werden können. Endpt \[ 0 \] . Ein wird nur signiert, wenn das Format ein vorsigniertes Format ist. Die anderen Endpunkte werden nur signiert, wenn der Endpunkt transformiert wurde oder wenn das Format ein signiertes Format ist. Der folgende Code veranschaulicht den Algorithmus zum Erweitern des Vorzeichens von Endpunktwerten mit zwei Regionen.

``` syntax
static void sign_extend_two_region(Pattern &p, IntEndpts endpts[NREGIONS_TWO])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
      if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
      if (p.transformed || BC6H::FORMAT == SIGNED_F16)
      {
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
        endpts[1].A[i] = SIGN_EXTEND(endpts[1].A[i], p.chan[i].delta[1]);
        endpts[1].B[i] = SIGN_EXTEND(endpts[1].B[i], p.chan[i].delta[2]);
      }
    }
}
```

Bei Kacheln mit einer Region ist das Verhalten identisch, nur wenn endpt \[ 1 \] entfernt wurde.

``` syntax
static void sign_extend_one_region(Pattern &p, IntEndpts endpts[NREGIONS_ONE])
{
    for (int i=0; i<NCHANNELS; ++i)
    {
    if (BC6H::FORMAT == SIGNED_F16)
        endpts[0].A[i] = SIGN_EXTEND(endpts[0].A[i], p.chan[i].prec);
    if (p.transformed || BC6H::FORMAT == SIGNED_F16) 
        endpts[0].B[i] = SIGN_EXTEND(endpts[0].B[i], p.chan[i].delta[0]);
    }
}
```

## <a name="transform-inversion-for-endpoint-values"></a>Transformationsinversion für Endpunktwerte

Bei Kacheln mit zwei Regionen wendet die Transformation die Umkehrung der Differenzcodierung an und fügt den Basiswert am Ende \[ 0 \] hinzu. Eine zu den drei anderen Einträgen für insgesamt 9 Add-Vorgänge. In der folgenden Abbildung wird der Basiswert als "A0" dargestellt und hat die höchste Gleitkommagenauigkeit. "A1", "B0" und "B1" sind Deltas, die aus dem Ankerwert berechnet werden, und diese Deltawerte werden mit geringerer Genauigkeit dargestellt. (A0 entspricht endpt \[ 0 \] . A, B0 entspricht endpt \[ 0 \] . B, A1 entspricht Endpt \[ 1 \] . A und B1 entsprechen Endpt \[ 1 \] .B.)

![Berechnung von Transformationsinversionsendpunktwerten](images/bc6h-transform-inverse.png)

Für Kacheln mit einer Region gibt es nur einen Deltaoffset und daher nur drei Hinzufügevorgänge.

Der Dekomprimator muss sicherstellen, dass die Ergebnisse der umgekehrten Transformation nicht die Genauigkeit von endpt \[ 0 \] .a überlaufen. Bei einem Überlauf müssen die Werte, die sich aus der umgekehrten Transformation ergeben, innerhalb der gleichen Anzahl von Bits umbrochen werden. Wenn die Genauigkeit von A0 "p" Bits ist, lautet der Transformationsalgorithmus:

`B0 = (B0 + A0) & ((1 << p) - 1)`

Bei Formaten mit Vorzeichen müssen die Ergebnisse der Deltaberechnung ebenfalls erweitert werden. Wenn der Vorgang der Vorzeichenerweiterung die Erweiterung beider Zeichen in Betracht zieht, wobei 0 positiv und 1 negativ ist, übernimmt die Vorzeichenerweiterung von 0 die obige Klammer. Entsprechend muss nach der obigen Klammer nur der Wert 1 (negativ) erweitert werden.

## <a name="unquantization-of-color-endpoints"></a>Nichtquantisierung von Farbendpunkten

Bei den nicht komprimierten Endpunkten besteht der nächste Schritt darin, eine anfängliche Aufhebung der Farbendpunkte durchzuführen. Dies umfasst drei Schritte:

-   Eine Nichtquantisierung der Farbpaletten
-   Interpolation der Paletten
-   Finalisierung der Nichtquantisierung

Durch das Aufteilen des Unquantisierungsprozesses in zwei Teile (Farbpalettenentquantisierung vor der Interpolation und endgültiges Aufheben der Äquantisierung nach der Interpolation) wird die Anzahl der Multiplikationsvorgänge reduziert, die im Vergleich zu einem vollständigen Nichtquantisierungsprozess vor der Paletteninterpolation erforderlich sind.

Der folgende Code veranschaulicht den Prozess zum Abrufen von Schätzungen der ursprünglichen 16-Bit-Farbwerte und zum anschließenden Verwenden der angegebenen Gewichtungswerte, um der Palette sechs zusätzliche Farbwerte hinzuzufügen. Der gleiche Vorgang wird auf jedem Kanal ausgeführt.

``` syntax
int aWeight3[] = {0, 9, 18, 27, 37, 46, 55, 64};
int aWeight4[] = {0, 4, 9, 13, 17, 21, 26, 30, 34, 38, 43, 47, 51, 55, 60, 64};

// c1, c2: endpoints of a component
void generate_palette_unquantized(UINT8 uNumIndices, int c1, int c2, int prec, UINT16 palette[NINDICES])
{
    int* aWeights;
    if(uNumIndices == 8)
        aWeights = aWeight3;
    else  // uNumIndices == 16
        aWeights = aWeight4;

    int a = unquantize(c1, prec); 
    int b = unquantize(c2, prec);

    // interpolate
    for(int i = 0; i < uNumIndices; ++i)
        palette[i] = finish_unquantize((a * (64 - aWeights[i]) + b * aWeights[i] + 32) >> 6);
}
```

Das nächste Codebeispiel veranschaulicht den Interpolationsprozess mit den folgenden Beobachtungen:

-   Da der vollständige Bereich der Farbwerte für die **Unquantize-Funktion** (unten) zwischen -32768 und 65535 liegt, wird der Interpolator mit 17-Bit-Arithmetik mit Vorzeichen implementiert.
-   Nach der Interpolation werden die Werte an die **\_ Finish-Funktion unquantize** übergeben (im dritten Beispiel in diesem Abschnitt beschrieben), die die endgültige Skalierung anwendet.
-   Alle Hardwaredekomprimierer sind erforderlich, um bitgenaue Ergebnisse mit diesen Funktionen zurückzugeben.

``` syntax
int unquantize(int comp, int uBitsPerComp)
{
    int unq, s = 0;
    switch(BC6H::FORMAT)
    {
    case UNSIGNED_F16:
        if(uBitsPerComp >= 15)
            unq = comp;
        else if(comp == 0)
            unq = 0;
        else if(comp == ((1 << uBitsPerComp) - 1))
            unq = 0xFFFF;
        else
            unq = ((comp << 16) + 0x8000) >> uBitsPerComp;
        break;

    case SIGNED_F16:
        if(uBitsPerComp >= 16)
            unq = comp;
        else
        {
            if(comp < 0)
            {
                s = 1;
                comp = -comp;
            }

            if(comp == 0)
                unq = 0;
            else if(comp >= ((1 << (uBitsPerComp - 1)) - 1))
                unq = 0x7FFF;
            else
                unq = ((comp << 15) + 0x4000) >> (uBitsPerComp-1);

            if(s)
                unq = -unq;
        }
        break;
    }
    return unq;
}
```

**Finish \_ unquantize** wird nach der Paletteninterpolation aufgerufen. Die **Unquantize-Funktion** verschiebt die Skalierung um 31/32 für signiert, 31/64 für nicht signiert. Dieses Verhalten ist erforderlich, um den endgültigen Wert in einen gültigen Halbbereich (-0x7BFF ~ 0x7BFF) zu bringen, nachdem die Paletteninterpolation abgeschlossen wurde, um die Anzahl der erforderlichen Multiplikationen zu reduzieren. **finish \_ unquantize** wendet die endgültige Skalierung an und gibt einen kurzen Wert ohne **Vorzeichen** zurück, der in die **hälfte** neu interpretiert wird.

``` syntax
unsigned short finish_unquantize(int comp)
{
    if(BC6H::FORMAT == UNSIGNED_F16)
    {
        comp = (comp * 31) >> 6;                                         // scale the magnitude by 31/64
        return (unsigned short) comp;
    }
    else // (BC6H::FORMAT == SIGNED_F16)
    {
        comp = (comp < 0) ? -(((-comp) * 31) >> 5) : (comp * 31) >> 5;   // scale the magnitude by 31/32
        int s = 0;
        if(comp < 0)
        {
            s = 0x8000;
            comp = -comp;
        }
        return (unsigned short) (s | comp);
    }
}
```

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Texturblockkomprimierung in Direct3D 11](texture-block-compression-in-direct3d-11.md)
</dt> </dl>

 

 