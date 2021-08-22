---
description: Eine ganze Zahl, die mit einer Eigenschaft mit den BitMap- und BitValue-Qualifizierern verknüpft ist.
ms.assetid: 14c34909-2419-41a1-a1ed-3b647a3c5e75
ms.tgt_platform: multiple
title: BitMap- und BitValue-Qualifizierer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48b02f2d9f2b6632d5f190d1537b2f33d822d916611983da71121ffbbded943d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051078"
---
# <a name="bitmap-and-bitvalue-qualifiers"></a>BitMap- und BitValue-Qualifizierer

Eine Bitmap ist eine ganze Zahl, die mit einer Eigenschaft mit den **BitMap-** und **BitValue-Qualifizierern** verknüpft ist. Jedes Bit des Eigenschaftswerts fungiert als Index für das Array von Werten in der **BitValue-Liste.** Da mehrere Bits im Eigenschaftswert gleichzeitig "on" sein können, ist es möglich, einen einzelnen Eigenschaftswert zu verwenden, um mehrere gleichzeitige Werte anzugeben.

Im folgenden MOF-Codebeispiel wird beispielsweise die **FileType-Eigenschaft** mit den **BitMap-** und **BitValues-Qualifizierern** eingerichtet. Außerdem wird festgelegt, dass das Bit mit niedriger Reihenfolge (Bit 0) dem Wert "Schreibgeschützt" entspricht. Das nächste Bit (Bit 1) entspricht "Hidden" usw. (Nicht alle Bits müssen signifikant sein. In diesem Acht-Bit-System haben die beiden hochwertigen Bits 6 und 7 keine Bedeutung.)

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

Wenn die **FileType-Eigenschaft** den Wert 7 (Bits 0000 0111) meldet, ist die Datei "Schreibgeschützte", "System" und "Ausgeblendet". Wenn die **FileType-Eigenschaft** den Wert 18 (0x12 Bits 0001 0010) meldet, handelt es sich um ein ausgeblendetes Unterverzeichnis.

Es gibt zwei verschiedene Arten von Bitmaps, die MOF-Code verwenden:

-   Aufeinanderfolgende signifikante Bits, die mit dem Bit mit niedriger Reihenfolge beginnen (Bit 0)

    Sie können ein Array von Bitwerten definieren, ohne explizit die signifikanten Bits anzugeben, wenn die signifikanten Bits mit dem Bit mit niedriger Reihenfolge (Bit 0) beginnen und ohne Unterbrechung durch alle Elemente im **BitValue-Array** nach oben gehen. Im folgenden MOF-Codebeispiel wird die gleiche Funktion wie im vorherigen Beispiel ausgeführt.

    ``` syntax
    [BitValues("Read Only",
               "Hidden",
               "System",
               "Volume Label",
               "Subdirectory",
               "Archive")]
    byte FileType;
    ```

-   Signifikantes Bit, dem ein nicht signifikantes Bit vorangestellt ist

    Wenn das Bit mit niedriger Reihenfolge nicht signifikant ist oder die Sequenz signifikanter Bits nicht kontinuierlich ist, müssen Sie sowohl die **BitMap-** als auch die **BitValues-Qualifizierer** angeben. Das folgende MOF-Codebeispiel zeigt eine Situation, in der das Bit mit niedriger Reihenfolge nicht signifikant ist und es eine Lücke in der Sequenz signifikanter Bits gibt.

    ``` syntax
    [BitMap("1","4","5"),
     BitValues("Follow-up","Delivery receipt","Read receipt")]
    sint32 MailOptions;
    ```

    In diesem Fall hat das Festlegen des Bits mit niedriger Reihenfolge (Bit 0) keine Bedeutung und wird ignoriert. Durch Festlegen von Bit 1 (0x2) wird jedoch angegeben, dass diese E-Mail-Nachricht für die Nachverfolgung gekennzeichnet ist. Durch Festlegen von Bit 4 (0x8) wird angegeben, dass ein Übermittlungsbeleg an den Absender gesendet werden soll, wenn die E-Mail-Nachricht beim Postfach des Empfängers eingetroffen ist. Durch Festlegen von Bit 5 (0x10) wird angegeben, dass ein Lesebeleg an den Absender gesendet werden soll, wenn die E-Mail-Nachricht vom Empfänger geöffnet wird. Durch Festlegen aller drei signifikanten Bits (0x1A) werden alle drei Bedingungen für die E-Mail-Nachricht angegeben.

## <a name="remarks"></a>Hinweise

Bestimmen Sie bei der Entscheidung, ob die **BitMap** / **BitValues-** oder **ValueMap** / **Values-Qualifizierer** verwendet werden sollen, ob einer der angegebenen Werte gleichzeitig auftreten kann. Wenn mehrere gleichzeitige Werte vorhanden sein können, müssen Sie **BitMap** / **BitValues** verwenden. Wenn sich alle Werte gegenseitig ausschließen, sollten Sie die **ValueMap** / **Values-Qualifizierer** verwenden.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ValueMap- und Wertqualifizierer](value-map.md)
</dt> </dl>

 

 



