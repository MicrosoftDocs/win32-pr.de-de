---
description: Gibt an, ob das Topologielader die von der Medienquelle bereitgestellten Medientypen aufzählt.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES -Attribut (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cc9ff7cf9e1497f0d15f68e68c254483f0c9f074e2ce4204e9d77d84aee4ea8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117691296"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a>\_MF-TOPOLOGIE \_ ENUMERATE \_ SOURCE \_ TYPES-Attribut

Gibt an, ob das Topologielader die von der Medienquelle bereitgestellten Medientypen aufzählt.

## <a name="data-type"></a>Datentyp

**UINT32**

Verwenden Sie einen der folgenden Werte.



| Wert                                                                                                                                    | Bedeutung                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE!</dt> </dl> | Enumerieren Sie die Quellmedientypen nicht.<br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE!</dt> </dl>    | Enumerieren Sie die Quellmedientypen.<br/>        |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut zu erhalten, rufen [**Sie DIE ATTRIBUTEs::GetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)

Rufen Sie ZUM Festlegen dieses [**Attributs DIE ATTRIBUTEs::SetUINT32 auf.**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)

## <a name="applies-to"></a>Gilt für:

[**TOPOLOGYTopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Hinweise

Jeder Stream in einer Medienquelle kann mehrere Medientypen bieten. Die Liste der Typen wird über die [**BESCHRIFTUNGMediaTypeHandler-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) für den Streamdeskriptor aufzählt.

Die Reihenfolge, in der das Topologielader versucht, die Medientypen einer Medienquelle zu verwenden, wird durch zwei Attribute gesteuert:

-   Das \_ \_ ENUMERATE SOURCE TYPES-Attribut der MF-TOPOLOGIE \_ in \_ der Topologie.
-   Das [**MF \_ TOPONODE \_ CONNECT \_ METHOD-Attribut**](mf-toponode-connect-method-attribute.md) auf dem Quellknoten.

Wenn das \_ \_ ENUMERATE SOURCE TYPES-Attribut der MF-TOPOLOGIE FALSE ist oder nicht festgelegt ist, verwendet das Topologielader den aktuellen \_ \_ Medientyp des  Streams. Die Liste der möglichen Typen wird nicht aufzählt. Wenn der aktuelle Medientyp nicht mit dem Downstreamtopologieknoten kompatibel ist und keine Kombination aus Decodern/Konvertern gefunden werden kann, schlägt die Topologieauflösung fehl.

Wenn das \_ \_ ENUMERATE SOURCE TYPES-Attribut der MF-TOPOLOGIE TRUE ist, werden vom Topologielader die Medientypen der Quelle aufzählt, bis ein kompatibler \_ \_ Typ gefunden wird.  In diesem Fall hängt die genaue Reihenfolge der Vorgänge davon ab, ob das [**MF \_ TOPONODE \_ CONNECT \_ METHOD-Attribut**](mf-toponode-connect-method-attribute.md) auf dem Quellknoten das **MF \_ CONNECT RESOLVE \_ INDEPENDENT \_ \_ OUTPUTTYPES-Flag** enthält.

Wenn MF TOPOLOGY ENUMERATE SOURCE TYPES auf TRUE festgelegt ist und das \_ \_ \_ \_ **MF \_ CONNECT RESOLVE \_ INDEPENDENT \_ \_ OUTPUTTYPES-Flag** festgelegt ist,  wird jeder Medientyp vom Topologielader wie folgt erschöpft, bevor zum nächsten übergelastet wird:

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

Wenn \_ \_ ENUMERATE SOURCE TYPES der \_ \_ MF-TOPOLOGIE **TRUE** ist, **aber MF \_ CONNECT RESOLVE \_ INDEPENDENT \_ \_ OUTPUTTYPES** nicht festgelegt ist, versucht das Topologielader eine direkte Verbindung mit jedem Medientyp, probiert dann jeden Medientyp mit Konvertern aus und versucht schließlich jeden Medientyp mit Decodern:

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

Wenn MF \_ TOPOLOGY \_ ENUMERATE SOURCE TYPES auf FALSE festgelegt ist, wird das \_ \_ **MF \_ CONNECT RESOLVE INDEPENDENT \_ \_ \_ OUTPUTTYPES-Flag** ignoriert. 

Der Standardwert von MF \_ TOPOLOGY \_ ENUMERATE SOURCE TYPES ist FALSE, um die Kompatibilität \_ mit vorhandenen Anwendungen zu \_ gewährleisten. 

Die GUID-Konstante für dieses Attribut wird aus mfuuid.lib exportiert.

### <a name="example"></a>Beispiel

Hier ist ein Beispiel, das das **MF \_ CONNECT RESOLVE INDEPENDENT \_ \_ \_ OUTPUTTYPES-Flag veranschaulicht.** Angenommen, für die Topologie ist das \_ MF-Topologieattribut \_ ENUMERATE \_ SOURCE TYPES auf TRUE \_ **festgelegt.**

Die Medienquelle bietet die folgenden Typen:

-   T1, T2, T3

Die Mediensenke akzeptiert die folgenden Typen:

-   T3, T4

Fall 1: Das **MF \_ CONNECT RESOLVE INDEPENDENT \_ \_ \_ OUTPUTTYPES-Flag** ist festgelegt.

1.  Das Topologielader versucht, eine direkte Verbindung mit T1 herzustellen. Die Senke lehnt T1 ab.
2.  Das Topologielader fügt einen Decoder ein, der T1 akzeptiert und T4 aus gibt. Die Senke akzeptiert T4.
3.  Die endgültige Topologie enthält: Medienquelle → Decoder → Mediensenke.

Fall 2: Das Flag ist nicht festgelegt.

1.  Das Topologielader versucht, eine direkte Verbindung mit T1 herzustellen. Die Senke lehnt T1 ab.
2.  Das Topologielader versucht, eine direkte Verbindung mit T2 herzustellen. Die Senke lehnt T2 ab.
3.  Das Topologielader versucht, eine direkte Verbindung mit T3 herzustellen. Die Senke akzeptiert T3.
4.  Die letzte Topologie enthält: Medienquelle → Mediensenke.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Alphabetische Liste Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




