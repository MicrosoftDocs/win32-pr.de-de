---
description: Definiert das Verhalten des Quellre resolvers. Diese Flags werden auch von Schemahandlern und Bytestreamhandlern verwendet.
ms.assetid: fe0b9090-5d2a-41a4-a806-57c874d3b3a2
title: Quellre konfliktlöserflags (Mfidl.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c779a54467390abf6cfb186f6b76043fd19617f5d129b88e6697a45c01708510
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119847820"
---
# <a name="source-resolver-flags"></a>Quellre konfliktlöserflags

Definiert das Verhalten des Quellre resolvers. Diese Flags werden auch von Schemahandlern und Bytestreamhandlern verwendet.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                                                                               | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_RESOLUTION_MEDIASOURCE"></span><span id="mf_resolution_mediasource"></span><dl> <dt>**MF \_ RESOLUTION \_ MEDIASOURCE**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                           | Versuchen Sie, eine Medienquelle zu erstellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| <span id="MF_RESOLUTION_BYTESTREAM"></span><span id="mf_resolution_bytestream"></span><dl> <dt>**MF \_ \_AUFLÖSUNGS-BYTESTREAM 0x00000002**</dt> <dt></dt> </dl>                                                                                                                                              | Versuchen Sie, einen Bytestream zu erstellen.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span id="MF_RESOLUTION_CONTENT_DOES_NOT_HAVE_TO_MATCH_EXTENSION_OR_MIME_TYPE_"></span><span id="mf_resolution_content_does_not_have_to_match_extension_or_mime_type_"></span><dl> <dt> **\_ MF-AUFLÖSUNGSINHALT \_ \_ MUSS NICHT MIT \_ \_ \_ \_ \_ ERWEITERUNGS- ODER \_ \_ \_ MIME-TYP-0X00000010**</dt> <dt></dt> </dl> | Wenn die Quellauflösung mit dem Bytestreamhandler fehlschlägt, der für den MIME-Typ oder die Dateierweiterung registriert ist, listet der Quellre resolver alle registrierten Bytestreamhandler auf.<br/> Bytestreamhandler werden nach Dateierweiterung oder MIME-Typ registriert. Zunächst versucht der Quellre resolver, einen Handler zu verwenden, der der Dateierweiterung oder dem MIME-Typ entspricht. Wenn dies fehlschlägt, schlägt standardmäßig die gesamte Quellauflösung fehl, und der Quellre resolver gibt einen Fehlercode an die Anwendung zurück. Wenn dieses Flag angegeben wird, listet der Quellre konfliktlöser jedoch weiterhin alle registrierten Bytestreamhandler auf. Möglicherweise kann ein handler mit falscher Übereinstimmung die Medienquelle erfolgreich erstellen.<br/> Dieses Flag kann nicht mit dem MF \_ RESOLUTION \_ KEEP \_ BYTE STREAM ALIVE ON \_ \_ \_ \_ FAIL-Flag kombiniert werden. Weitere Informationen finden Sie unter Hinweise.<br/> |
| <span id="MF_RESOLUTION_KEEP_BYTE_STREAM_ALIVE_ON_FAIL"></span><span id="mf_resolution_keep_byte_stream_alive_on_fail"></span><dl> <dt>**MF \_ AUFLÖSUNG \_ KEEP \_ BYTE STREAM ALIVE ON \_ \_ \_ \_ FAIL**</dt> <dt>0X00000020</dt> </dl>                                                                             | Wenn bei der Quellauflösung ein Fehler auftritt, schließt der Quellre resolver den Bytestream nicht. Standardmäßig schließt der Quellre resolver den Bytestream bei einem Fehler.<br/> Wenn dieses Flag verwendet wird und bei der Quellauflösung ein Fehler auftritt, sollte der Aufrufer die -Methode erneut aufrufen und das Flag MF \_ RESOLUTION CONTENT DOES NOT HAVE TO MATCH EXTENSION OR \_ MIME TYPE \_ \_ \_ \_ \_ \_ \_ \_ \_ festlegen.<br/> Dieses Flag kann nicht mit dem FLAG MF \_ RESOLUTION CONTENT DOES NOT MATCH EXTENSION OR \_ MIME TYPE \_ kombiniert \_ \_ \_ \_ \_ \_ \_ \_ werden. Weitere Informationen finden Sie unter Hinweise.<br/>                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="MF_RESOLUTION_READ"></span><span id="mf_resolution_read"></span><dl> <dt>**MF \_ RESOLUTION \_ READ**</dt> <dt>0X00010000</dt> </dl>                                                                                                                                                                | Fordert Lesezugriff auf die Quelle an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MF_RESOLUTION_WRITE"></span><span id="mf_resolution_write"></span><dl> <dt>**MF \_ \_AUFLÖSUNGS-0X00020000**</dt> <dt></dt> </dl>                                                                                                                                                             | Fordert Schreibzugriff auf die Quelle an.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="MF_RESOLUTION_DISABLE_LOCAL_PLUGINS"></span><span id="mf_resolution_disable_local_plugins"></span><dl> <dt>**MF \_ AUFLÖSUNG \_ DEAKTIVIEREN SIE LOKALE \_ \_ PLUG-INS**</dt> <dt>0X00000040</dt> </dl>                                                                                                           | Der Quellre resolver verwendet keine lokal registrierten Schema- oder Bytestreamhandler-Plug-Ins.<br/> Erfordert Windows 8.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="remarks"></a>Hinweise

Die Anwendung legt diese Flags fest, wenn sie die [**BENUTZEROBERFLÄCHESourceResolver-Schnittstelle**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver) verwendet. Der Quellre resolver übergibt die gleichen Flags an die METHODEN 2016 UND 2016 [**AN DIE METHODEN 2016 UND 2016.**](/windows/desktop/api/mfidl/nf-mfidl-imfbytestreamhandler-begincreateobject) [](/windows/desktop/api/mfidl/nf-mfidl-imfschemehandler-begincreateobject)

Sie müssen eines der MF \_ RESOLUTION \_ MEDIASOURCE- oder MF \_ RESOLUTION \_ BYTESTREAM-Flags angeben. Die verbleibenden Flags sind alle optional.

Das MF \_ RESOLUTION \_ KEEP \_ BYTE STREAM ALIVE ON \_ \_ \_ \_ FAIL-Flag ist für das folgende Szenario definiert:

1.  Die Anwendung versucht, eine Quelle über das Netzwerk zu öffnen. Die Anwendung legt das Flag MF \_ RESOLUTION \_ KEEP \_ BYTE STREAM ALIVE ON \_ \_ FAIL \_ \_ fest.

2.  Die URL der Quelle enthält die falsche Dateierweiterung. Da die Dateierweiterung falsch ist, kann der Standardmäßige Bytestreamhandler die Medienquelle nicht erstellen. Da die Anwendung das Flag MF RESOLUTION KEEP BYTE STREAM ALIVE ON FAIL festgelegt hat, speichert der Quellre \_ \_ \_ \_ \_ \_ \_ resolver den Bytestream zwischen.

3.  Der Quellre resolver gibt einen Fehlercode an die Anwendung zurück.

4.  Der Client öffnet die Quelle erneut. Dieses Mal muss das Flag MF RESOLUTION CONTENT DOES NOT MATCH EXTENSION OR MIME TYPE (MF-AUFLÖSUNGSINHALT MUSS NICHT MIT ERWEITERUNG \_ \_ ODER \_ \_ \_ \_ \_ \_ \_ \_ \_ MIME-TYP ÜBEREINSTIMMEN) festlegen. Dieses Flag bewirkt, dass der Quellre resolver alle registrierten Handler anstelle des Standardhandlers versucht. Da der Bytestream zwischengespeichert wurde, muss der Quellre resolver den Bytestream nicht erneut öffnen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Mfidl.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Media Foundation Konstanten](media-foundation-constants.md)
</dt> <dt>

[**VERERBByteStreamHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfbytestreamhandler)
</dt> <dt>

[**VERERBungshandler**](/windows/desktop/api/mfidl/nn-mfidl-imfschemehandler)
</dt> <dt>

[**VERERBUNGQuelleResolver**](/windows/desktop/api/mfidl/nn-mfidl-imfsourceresolver)
</dt> <dt>

[Quellre resolver](source-resolver.md)
</dt> </dl>

 

 




