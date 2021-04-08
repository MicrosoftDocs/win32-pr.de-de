---
description: Definiert das Verhalten des Quell Resolvers. Diese Flags werden auch von Schema Handlern und Byte Datenstrom Handlern verwendet.
ms.assetid: fe0b9090-5d2a-41a4-a806-57c874d3b3a2
title: Quellresolverflags (MFI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 31efe47f75151f78958903cb514653edb6c5aa08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103753857"
---
# <a name="source-resolver-flags"></a>Quellresolver-Flags

Definiert das Verhalten des Quell Resolvers. Diese Flags werden auch von Schema Handlern und Byte Datenstrom Handlern verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_RESOLUTION_MEDIASOURCE"></span><span id="mf_resolution_mediasource"></span><dl> <dt>**MF \_ Resolution \_ MediaSource**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                           | Es wurde versucht, eine Medienquelle zu erstellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="MF_RESOLUTION_BYTESTREAM"></span><span id="mf_resolution_bytestream"></span><dl> <dt>**MF \_ Auflösung \_ Bytestream**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                              | Es wurde versucht, einen Bytestream zu erstellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="MF_RESOLUTION_CONTENT_DOES_NOT_HAVE_TO_MATCH_EXTENSION_OR_MIME_TYPE_"></span><span id="mf_resolution_content_does_not_have_to_match_extension_or_mime_type_"></span><dl> Der <dt> **MF- \_ Auflösungs \_ Inhalt \_ \_ \_ muss nicht mit der \_ \_ \_ Erweiterung oder dem MIME- \_ \_ \_ Typ**</dt> <dt>0x00000010</dt> identisch sein. </dl> | Wenn die Quell Auflösung mit dem Byte Datenstrom Handler fehlschlägt, der für den MIME-Typ oder die Dateinamenerweiterung registriert ist, listet der quellresolver alle registrierten Byte-Stream-Handler auf.<br/> Bytestreamhandler werden durch die Dateinamenerweiterung oder den MIME-Typ registriert. Anfänglich versucht der quellresolver, einen Handler zu verwenden, der mit der Dateinamenerweiterung oder dem MIME-Typ übereinstimmt. Wenn dies nicht möglich ist, schlägt die gesamte Quell Auflösung standardmäßig fehl, und der quellresolver gibt einen Fehlercode an die Anwendung zurück. Wenn dieses Flag angegeben wird, listet der quellresolver weiterhin alle registrierten Byte-Stream-Handler auf. Möglicherweise kann ein falsch passender Handler die Medienquelle erfolgreich erstellen.<br/> Dieses Flag kann nicht mit der MF-Auflösung kombiniert werden, bei der das Flag zum Ausführen eines \_ \_ \_ \_ Bytestreams \_ \_ in Byte \_ Weitere Informationen finden Sie unter Hinweise.<br/> |
| <span id="MF_RESOLUTION_KEEP_BYTE_STREAM_ALIVE_ON_FAIL"></span><span id="mf_resolution_keep_byte_stream_alive_on_fail"></span><dl> <dt>**MF \_ Auflösung \_ \_ von Byte \_ Daten \_ Strom \_ bei \_**</dt> Fehler " <dt>0x00000020</dt> " beibehalten </dl>                                                                             | Wenn die Quell Auflösung fehlschlägt, schließt der quellresolver den Bytestream nicht. Standardmäßig schließt der Quell Konflikt Löser den Bytestream bei einem Fehler.<br/> Wenn dieses Flag verwendet wird und die Quell Auflösung fehlschlägt, sollte der Aufrufer die Methode erneut anrufen und festlegen, dass der MF- \_ Auflösungs \_ Inhalt \_ \_ nicht \_ mit der \_ \_ \_ Erweiterung oder dem \_ MIME- \_ \_ Typflag identisch sein muss.<br/> Dieses Flag kann nicht mit dem MF- \_ Auflösungs Inhalt kombiniert werden, der dem \_ Erweiterungs- \_ \_ \_ \_ \_ \_ \_ oder MIME- \_ \_ Typflag nicht entspricht. Weitere Informationen finden Sie unter Hinweise.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="MF_RESOLUTION_READ"></span><span id="mf_resolution_read"></span><dl> <dt>**MF \_ Auflösung \_ gelesen**</dt> <dt>0x00010000 bis</dt> </dl>                                                                                                                                                                | Fordert Lesezugriff auf die Quelle an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MF_RESOLUTION_WRITE"></span><span id="mf_resolution_write"></span><dl> <dt>**MF \_ Auflösung \_ Schreiben**</dt> <dt>0x00020000</dt> </dl>                                                                                                                                                             | Fordert Schreibzugriff auf die Quelle an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="MF_RESOLUTION_DISABLE_LOCAL_PLUGINS"></span><span id="mf_resolution_disable_local_plugins"></span><dl> <dt>**MF \_ Auflösung \_ Deaktivieren \_ der \_ lokalen**</dt> Plug-Ins <dt>0x00000040</dt> </dl>                                                                                                           | Der quellresolver verwendet nicht lokal registrierte Schemas oder Bytestream-Handler-Plug-ins.<br/> Erfordert Windows 8.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="remarks"></a>Bemerkungen

Diese Flags werden von der Anwendung festgelegt, wenn Sie die [**IMF sourceresolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) -Schnittstelle verwendet. Der quellresolver übergibt dieselben Flags an die [**imfbytestreamhandler:: beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) -und [**imfschemehandler:: beginkreateobject**](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject) -Methoden.

Sie müssen eine der Lösungen für die MF- \_ Auflösung \_ MediaSource oder MF \_ Resolution \_ Bytestream angeben. Die restlichen Flags sind optional.

Das Flag für die MF-Auflösung, bei dem der \_ \_ Byte Datenstrom aktiv ist, \_ \_ \_ \_ \_ wird für das folgende Szenario definiert:

1.  Die Anwendung versucht, eine Quelle über das Netzwerk zu öffnen. Die Anwendung legt die MF- \_ Auflösung fest \_ \_ \_ \_ \_ \_

2.  Die URL der Quelle enthält die falsche Dateinamenerweiterung. Da die Dateinamenerweiterung falsch ist, kann die Medienquelle vom standardmäßigen Byte Datenstrom Handler nicht erstellt werden. Da die Anwendung die MF- \_ Auflösung festgelegt \_ \_ \_ \_ \_ \_ hat, wird der Bytestream von der Quell Auflösung zwischengespeichert.

3.  Der quellresolver gibt einen Fehlercode an die Anwendung zurück.

4.  Der Client öffnet die Quelle erneut. dieses Mal muss der Inhalt der MF- \_ Auflösung \_ \_ \_ nicht \_ mit der \_ \_ \_ Erweiterung \_ oder dem \_ MIME- \_ Typflag identisch sein. Dieses Flag bewirkt, dass der quellresolver anstelle des Standard Handler alle registrierten Handler ausprobiert. Da der Bytestream zwischengespeichert wurde, muss der byteresolver den Bytestream nicht erneut öffnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mspdl. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> <dt>

[**IMF bytestreamhandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
</dt> <dt>

[**IMF Schema Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)
</dt> <dt>

[**IMF sourceresolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> <dt>

[Quellresolver](source-resolver.md)
</dt> </dl>

 

 




