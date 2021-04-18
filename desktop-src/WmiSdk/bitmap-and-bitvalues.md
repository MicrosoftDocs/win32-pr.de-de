---
description: Eine ganze Zahl, die mit der Bitmap-und BitValue-Qualifizierer mit einer Eigenschaft verknüpft ist.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: Bitmap-und BitValue-Qualifizierer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60dd6b4ad5866ddc79c960316757700bc5fbb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358820"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a>Bitmap-und BitValue-Qualifizierer

Eine Bitmap ist eine Ganzzahl, die mit einer Eigenschaft verknüpft ist, die die **Bitmap** -und **BitValue** -Qualifizierer Jedes Bit des Eigenschafts Werts fungiert als Index in das Array von Werten in der **BitValue** -Liste. Da mehrere Bits im Eigenschafts Wert gleichzeitig "on" sein können, kann ein einzelner Eigenschafts Wert verwendet werden, um mehrere gleichzeitige Werte anzugeben.

Beispielsweise wird mit dem folgenden MOF-Codebeispiel die **filetype** -Eigenschaft so eingerichtet, dass Sie über die Qualifizierer **Bitmap** und **BitValues** verfügt. Außerdem wird festgelegt, dass das niedrig wertige Bit (Bit 0) dem Wert "Read only" entspricht. Das nächste Bit (Bit 1) entspricht "Hidden" usw. (Nicht alle Bits müssen von Bedeutung sein. In diesem 8-Bit-System haben die zwei hohen Bestell Bits (6 und 7) keine Bedeutung.)

``` syntax
[BitMap("0","1","2","3","4","5"),
 BitValues("Read Only",
           "Hidden",
           "System",
           "Volume Label",
           "Subdirectory",
           "Archive")]
byte FileType;
```

Wenn die **filetype** -Eigenschaft den Wert 7 (Bits 0000 0111) meldet, ist die Datei "Read only", "System" und "Hidden". Wenn die **filetype** -Eigenschaft den Wert 18 (0x12, Bits 0001 0010) meldet, ist es ein verborgenes Unterverzeichnis.

Es gibt zwei verschiedene Typen von Bitmaps, die MOF-Code verwenden:

-   Aufeinanderfolgende bedeutende Bits, beginnend mit dem nieder wertigen Bit (Bit 0)

    Sie können ein Array von Bitwerten definieren, ohne die signifikanten Bits explizit anzugeben, wenn die signifikanten Bits mit dem unteren Bit (Bit 0) beginnen, und der Fortschritt ohne Unterbrechung durch alle Elemente im **BitValue** -Array. Im folgenden MOF-Codebeispiel wird die gleiche Funktion wie im vorherigen Beispiel durchführt.

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   Signifikanter Bit, dem ein nicht signifikanter Bit vorangestellt ist

    Wenn das niedrig wertige Bit unerheblich ist oder die Sequenz signifikanter Bits nicht fortlaufend ist, müssen Sie sowohl die **Bitmap** -als auch die **BitValues** -Qualifizierer angeben. Das folgende MOF-Codebeispiel zeigt eine Situation, in der das Bit mit niedriger Ordnung nicht signifikant ist und eine Lücke in der Sequenz signifikanter Bits vorliegt.

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    In diesem Fall hat das Festlegen des nieder wertigen Bits (Bit 0) keine Bedeutung und wird ignoriert. Durch Festlegen von Bit 1 (0x2) wird jedoch angegeben, dass diese e-Mail-Nachricht für die Nachverfolgung gekennzeichnet ist. durch Festlegen von Bit 4 (0x8) wird angegeben, dass eine Übermittlungs Bestätigung an den Absender gesendet werden soll, wenn die e-Mail-Nachricht im Postfach des Empfängers eingetroffen ist. durch Festlegen von Bit 5 (0x10) wird angegeben, dass eine Lesebestätigung an den Absender gesendet werden soll, wenn die e-Mail-Nachricht vom Empfänger geöffnet wird. Durch Festlegen aller drei signifikanten Bits (0x1A) werden alle drei Bedingungen für die e-Mail-Nachricht angegeben.

## <a name="remarks"></a>Bemerkungen

Wenn Sie entscheiden, ob Sie die **Bitmap**- / **Bitwerte** oder **ValueMap** / **Values** -Qualifizierer verwenden möchten, stellen Sie fest, ob einer der aufgeführten Werte gleichzeitig auftreten könnte. Wenn mehrere gleichzeitige Werte vorhanden sein können, müssen **Bitmap**- / **Bitwerte** verwendet werden. Wenn sich alle Werte gegenseitig ausschließen, sollten Sie die **ValueMap** / **Values** -Qualifizierer verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ValueMap-und Wert Qualifizierer](value-map.md)
</dt> </dl>

 

 



