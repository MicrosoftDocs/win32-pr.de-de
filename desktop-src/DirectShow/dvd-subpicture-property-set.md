---
description: Dvd-Unterbildeigenschaften steuern die Farbe, den Kontrast und die Ausgabe der Unterbildanzeige.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: DVD Subpicture-Eigenschaftensatz (Dvdmedia.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293e38665fc59cf47b44e6466302655afd2ccf2a909034afd803201f6ea5a78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148693"
---
# <a name="dvd-subpicture-property-set"></a>DVD Subpicture-Eigenschaftensatz

Dvd-Unterbildeigenschaften steuern die Farbe, den Kontrast und die Ausgabe der Unterbildanzeige.

Die folgenden Informationen stellen die erforderlichen Konstanten und Datentypen dar, die für diesen Eigenschaftensatz in Aufrufen von [**IKsPropertySet-Methoden**](ikspropertyset.md) verwendet werden sollen. Sie stellt Werte für die **Parameter GUID** (*guidPropSet),* Eigenschaften-ID (*dwPropID*) und Eigenschaftendatentyp (*pPropData*) bereit.



| Bezeichnung | Wert |
|-------------------|----------------------------|
| Eigenschaftensatz-GUID | AM \_ KSPROPSETID \_ DvdSubPic |



 



| Eigenschafts-ID                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_AM-EIGENSCHAFT \_ DVDSUBPIC \_ COMPOSIT \_ ON | Nur festlegende Eigenschaft, die die Anzeige der Unterbildanzeige aktiviert oder deaktiviert. DirectShow definiert den booleschen AM **\_ PROPERTY \_ COMPOSIT \_ ON-Datentyp** für diese Eigenschaft sowie PAM \_ PROPERTY \_ COMPOSIT \_ ON als Zeiger auf diesen Datentyp. **TRUE** gibt an, dass das Teilbild angezeigt wird, **FALSE** gibt an, dass es deaktiviert wird. Weitere Informationen finden Sie im WDM-Teil des Windows DDK. |
| AM \_ PROPERTY \_ DVDSUBPIC \_ HLI          | Nur festlegende Eigenschaft, die ein Rechteck aus Bildunterdrückung oder Bildschirm angibt, dessen Farbe oder Kontrast geändert wird. Der Datentyp ist [**AM \_ PROPERTY \_ SPHLI.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) Siehe Hinweise.                                                                                                                                                                                |
| AM \_ PROPERTY \_ DVDSUBPIC \_ PALETTE      | Legt die Palette für ein Teilbild fest. Der Datentyp ist [**AM \_ PROPERTY \_ SPPAL.**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal)                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Hinweise

Die **EIGENSCHAFT AM PROPERTY \_ \_ DVDSUBPIC \_ HLI** ist nur festgelegt. Sie gibt ein Rechteck aus Bildunterdrückung oder Bildschirm an, dessen Farbe oder Kontrast geändert wird. Dies unterscheidet sich von der DVD-Video-Spezifikation, da der Microsoft DVD-Navigator alle Schaltflächen- und Tastaturinformationen analysiert und immer nur ein Hervorhebungsrechteck an den Unterbilddecoder übergibt. Daher werden Hervorhebungsinformationen häufiger an den Decoder gesendet, als sie im DVD-Stream vorhanden sind.

Die Hervorhebungsinformationen gelangen asynchron zum Datenstrom. Der Decoder verwendet die Zeitstempel start und end, um die Hervorhebungsinformationen ggf. mit den relevanten Bildbildinformationen zu korrelieren. Wenn der Decoder keine Subpicture-Datenstrominformationen für die angeforderten Zeitstempel empfangen hat, geht der Decoder davon aus, dass die Hervorhebungsinformationen eigenständig sind und nicht für eine Unterbildung gelten. In diesem Fall geht der Decoder davon aus, dass die Farb- und Kontrastinformationen die gleiche Farbe haben.

Die Daten befinden sich nicht vollständig im DVD-Datenträgerformat. Microsoft stellt eine zusätzliche Struktur vom Typ [**AM \_ PROPERTY \_ SPHLI**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) bereit, die als Parameter an diese Eigenschaft übergeben wird. Diese Struktur beschreibt die aktuell ausgewählte Schaltfläche aus den Dvd-Hervorhebungsinformationen.

Der DVD-Navigator verarbeitet alle Tastatureingabeinformationen und sendet bei jeder Änderung eines Schaltflächenzustands neue Hervorhebungsinformationen. Die Informationen beschreiben jeweils nur einen Modus von einer Schaltfläche. Sie enthält ein Anzeigerechteck in Pixelkoordinaten des Bildschirms oder ggf. eine Anzeige der Bildfläche. Die Struktur enthält auch Farb- und Kontrastinformationen, jedoch nur für den aktuellen Zustand der aktuell ausgewählten Schaltfläche. Das Format wird in der DVD-Spezifikation definiert.

Hervorhebungsinformationen enthalten Start- und Endzeitstempel. Diese befinden sich in den gleichen Einheiten wie andere Zeitstempel, mit zwei Ausnahmen: Ein Startzeitstempel von 0xFFFFFFFF bedeutet, dass die Highlight-Eigenschaft beim Empfang wirksam ist, und ein Endzeitstempel von 0xFFFFFFFF bedeutet, dass die Hervorhebungseigenschaft gültig ist, bis die nächste Hervorhebung empfangen wird.

Das HLISS-Feld ist in der DVD-Spezifikation definiert. Der Wert 0 gibt an, dass alle Hervorhebungen ungültig sind, und der Decoder sollte alle Hervorhebungen deaktivieren.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




