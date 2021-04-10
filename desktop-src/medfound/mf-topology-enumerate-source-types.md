---
description: Gibt an, ob der topologielader die Medientypen auflistet, die von der Medienquelle bereitgestellt werden.
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343309"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a>MF- \_ \_ topologieaufzählenden \_ Quell \_ Typen Attribut

Gibt an, ob der topologielader die Medientypen auflistet, die von der Medienquelle bereitgestellt werden.

## <a name="data-type"></a>Datentyp

**UINT32**

Verwenden Sie einen der folgenden Werte.



| Wert                                                                                                                                    | Bedeutung                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <dt>FALSE * * * *</dt> </dl> | Zählen Sie nicht die Quell Medientypen auf.<br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <dt>TRUE * * * *</dt> </dl>    | Listet die Quell Medientypen auf.<br/>        |



 

## <a name="getset"></a>Abrufen/Festlegen

Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).

Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).

## <a name="applies-to"></a>Gilt für:

[**Imftopology**](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a>Bemerkungen

Jeder Datenstrom in einer Medienquelle kann mehr als einen Medientyp anbieten. Die Liste der Typen wird durch die [**imvmediatyethandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) -Schnittstelle auf dem Datenstrom Deskriptor aufgezählt.

Die Reihenfolge, in der der topologielader versucht, die Medientypen einer Medienquelle zu steuern, wird durch zwei Attribute gesteuert:

-   Die MF- \_ Topologie \_ listet das \_ Quell \_ Typen Attribut in der Topologie auf.
-   Das [**MF \_ toponode \_ Connect \_ method**](mf-toponode-connect-method-attribute.md) -Attribut auf dem Quellknoten.

Wenn das \_ Attribut für die MF-topologieenumeration \_ \_ Quell Typen auf \_ **false** festgelegt oder nicht festgelegt ist, verwendet das topologielader den aktuellen Medientyp des Streams. Die Liste der möglichen Typen wird nicht aufgelistet. Wenn der aktuelle Medientyp nicht mit dem Knoten der Downstream-Topologie kompatibel ist und keine Kombination aus Decodern/Konvertern gefunden werden kann, tritt bei der topologieauflösung ein Fehler auf.

Wenn das Attribut für die MF- \_ topologieaufzählenden \_ Quell Typen den Wert \_ \_ **true** hat, listet das topologielader die Medientypen der Quelle auf, bis ein kompatibler Typ gefunden wird. In diesem Fall hängt die genaue Reihenfolge der Vorgänge davon ab, ob das [**MF \_ toponode \_ Connect \_ method**](mf-toponode-connect-method-attribute.md) -Attribut auf dem Quellknoten das **MF \_ Connect \_ Resolve \_ Independent \_ OutputTypes** -Flag enthält.

Wenn die MF \_ -Topologie \_ aufzählenden \_ Quell \_ Typen auf **true** festgelegt ist und das **MF \_ Connect \_ Resolve \_ Independent \_ OutputTypes** -Flag festgelegt ist, werden die einzelnen Medientypen vom topologielader vor der Umstellung auf den nächsten in der folgenden Form erschöpft:

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

Wenn die MF- \_ Topologie " \_ true" aufzählt, \_ \_ aber **MF \_ Connect \_ \_ unabhängige \_ OutputTypes** nicht festgelegt ist, versucht das topologielader eine direkte Verbindung mit jedem Medientyp, versucht dann jeden Medientyp mit Konvertern zu versuchen und schließlich jeden Medientyp mit Decodern  zu versuchen:

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

Wenn die MF- \_ Topologie \_ aufzählenden \_ Quell \_ Typen den Wert **false** hat, wird das kennflag für die **MF \_ Connect \_ Resolve \_ Independent \_ OutputTypes** ignoriert.

Der Standardwert der MF- \_ Topologie \_ Enumerate \_ Source \_ types ist **false**, um die Kompatibilität mit vorhandenen Anwendungen zu erhalten.

Die GUID-Konstante für dieses Attribut wird aus "mfuuid. lib" exportiert.

### <a name="example"></a>Beispiel

Im folgenden Beispiel wird das Flag " **MF \_ Connect \_ Resolve \_ Independent \_ OutputTypes** " veranschaulicht. Angenommen, in der Topologie ist das Attribut für die MF- \_ Topologie \_ Enumerate \_ Source \_ types auf **true** festgelegt.

Die Medienquelle bietet die folgenden Typen:

-   T1, T2, T3

Die Medien Senke akzeptiert die folgenden Typen:

-   T3, T4

Fall 1: das Flag " **MF \_ Connect \_ Resolve \_ Independent \_ OutputTypes** " wurde festgelegt.

1.  Das topologielader versucht, eine direkte Verbindung mit T1 herzustellen. Die Senke lehnt T1 ab.
2.  Das topologielader fügt einen Decoder ein, der T1 annimmt und T4 ausgibt. Die Senke akzeptiert T4.
3.  Die letzte Topologie enthält: Medienquelle → Decoder → Medien Senke.

Fall 2: das Flag ist nicht festgelegt.

1.  Das topologielader versucht, eine direkte Verbindung mit T1 herzustellen. Die Senke lehnt T1 ab.
2.  Das topologielader versucht, eine direkte Verbindung mit T2 herzustellen. Die Senke lehnt T2 ab.
3.  Das topologielader versucht, eine direkte Verbindung mit T3 herzustellen. Die Senke akzeptiert T3.
4.  Die letzte Topologie enthält: Medienquelle → Medien Senke.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                            |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Alphabetische Liste der Media Foundation Attribute](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Topologieattribute](topology-attributes.md)
</dt> </dl>

 

 




