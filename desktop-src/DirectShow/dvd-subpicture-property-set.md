---
description: Die Eigenschaften des DVD-Teil Bilds steuern die Farbe, den Kontrast und die Ausgabe der Anzeige des unter Bilds.
ms.assetid: ddbfb65c-7630-4e9f-8013-c5d65c62c628
title: Eigenschaften Satz des DVD-Teil Bilds (dvdmedia. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac2706bd0a7f078fb7352e70e8f8eb62f5dea948
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371166"
---
# <a name="dvd-subpicture-property-set"></a>Eigenschaften Satz des DVD-Teil Bilds

Die Eigenschaften des DVD-Teil Bilds steuern die Farbe, den Kontrast und die Ausgabe der Anzeige des unter Bilds.

Die folgenden Informationen stellen die erforderlichen Konstanten und Datentypen dar, die für diesen Eigenschaften Satz in Aufrufen von " [**ikspropertyset**](ikspropertyset.md) "-Methoden verwendet werden. Es werden Werte für die Parameter **GUID** (*guidpropset*), Property ID (*dwpropid*) und Property Data Type (*ppropdata*) bereitstellt.



|                   |                            |
|-------------------|----------------------------|
| Eigenschaftensatz-GUID | AM \_ kspropabtid \_ dvdsubpic |



 



| Eigenschafts-ID                           | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| am- \_ Eigenschaft \_ dvdsubpic \_ Composit \_ on | Nur festgelegte Eigenschaft, die die Anzeige von Teil Bildern aktiviert oder deaktiviert. DirectShow definiert das **am- \_ Eigenschafts \_ Composit \_** für den booleschen Datentyp für diese Eigenschaft sowie die PAM- \_ Eigenschaft \_ Composit \_ als Zeiger auf diesen Datentyp. **True** gibt an, dass das Unterbild angezeigt wird, **false** gibt an, dass es deaktiviert Weitere Informationen finden Sie im WDM-Teil des Windows-DDK. |
| AM- \_ Eigenschaft \_ dvdsubpic \_ HLI          | Nur festgelegte Eigenschaft, die ein Rechteck eines unter Bilds oder eines Bildschirms angibt, dessen Farbe oder Kontrast geändert wird. Der Datentyp ist die [**\_ Eigenschaft \_ sphli**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli). Siehe Hinweise.                                                                                                                                                                                |
| AM- \_ Eigenschaft ( \_ dvdsubpic- \_ Palette)      | Legt die Palette für ein Teilbild fest. Der Datentyp ist die [**\_ Eigenschaft \_ sppal**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sppal).                                                                                                                                                                                                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Die Eigenschaft "an **\_ Eigenschaft \_ dvdsubpic \_ HLI** " ist nur festgelegt. Es gibt ein Rechteck mit einem unter Bild oder Bildschirm an, dessen Farbe oder Kontrast geändert wird. Dies unterscheidet sich von der DVD-Video Spezifikation, da der Microsoft DVD Navigator alle Schaltflächen-und Tastatur Informationen analysiert und jeweils nur ein Hervorhebungs Rechteck an den Teil Bild Decoder übergibt. Daher werden Hervorhebungs Informationen häufiger an den Decoder gesendet, als Sie im DVD-Stream vorhanden sind.

Die Hervorhebungs Informationen werden asynchron in den Datenstrom gelangt. Der Decoder verwendet die Hervorhebungs-und Endzeit Stempel, um die Hervorhebungs Informationen mit den entsprechenden Teil Bildinformationen zu korrelieren, falls vorhanden. Wenn der Decoder keine unter bildstreaminformationen für die angeforderten Zeitstempel erhalten hat, geht der Decoder davon aus, dass die Hervorhebungs Informationen eigenständig sind und nicht auf ein Teilbild angewendet werden. In diesem Fall geht der Decoder davon aus, dass die Farbe und die Kontrast Informationen identisch sind.

Die Daten sind nicht vollständig im DVD-Festplatten Format enthalten. Microsoft stellt eine zusätzliche Struktur des Typs " [**am \_ Property \_ sphli**](/previous-versions/windows/desktop/api/Dvdmedia/ns-dvdmedia-am_property_sphli) " bereit, die als Parameter an diese Eigenschaft übergeben wird. Diese Struktur beschreibt die aktuell ausgewählte Schaltfläche aus den Informationen zur DVD-Hervorhebung.

Der DVD-Navigator verarbeitet alle Tastatureingabe-Informationen und sendet bei jeder Änderung eines Schaltflächen Zustands neue Hervorhebungs Informationen. Die Informationen beschreiben jeweils nur einen Modus für eine Schaltfläche. Sie enthält ein Anzeige Rechteck in Pixelkoordinaten des Bildschirms oder eine Anzeige des unter Bilds, falls vorhanden. Die Struktur enthält auch Farb-und Kontrast Informationen, jedoch nur für den aktuellen Zustand der aktuell ausgewählten Schaltfläche. Das Format wird in der DVD-Spezifikation definiert.

Die Hervorhebungs Informationen enthalten Zeitstempel für Start und Ende. Diese befinden sich in den gleichen Einheiten wie andere Zeitstempel, mit zwei Ausnahmen: ein Start Zeitstempel von 0xFFFFFFFF bedeutet, dass die Hervorhebungs Eigenschaft beim Empfang wirksam ist, und ein Endzeit Stempel von 0xFFFFFFFF bedeutet, dass die Hervorhebungs Eigenschaft gültig ist, bis die nächste Hervorhebung empfangen wurde.

Das hliss-Feld ist wie in der DVD-Spezifikation definiert. Der Wert 0 (null) gibt an, dass alle Highlights ungültig sind und der Decoder alle Highlights deaktivieren soll.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|---------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Dvdmedia. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaftensätze](property-sets.md)
</dt> </dl>

 

 




