---
description: Bearbeitet eine Text Konferenzbeschreibung.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Itconferendceblob-Schnittstelle (sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352999"
---
# <a name="itconferenceblob-interface"></a>Itconferendceblob-Schnittstelle

\[ Rendezvous-Steuerelemente und Schnittstellen für die IP-telefoniekonferenz sind nicht für die Verwendung in Windows Vista, Windows Server 2008 und nachfolgenden Versionen des Betriebssystems verfügbar. Die RTC-Client-API bietet eine ähnliche Funktionalität.\]

Die **itconferenceblob** -Schnittstelle bearbeitet eine Text Konferenzbeschreibung. Die-Schnittstelle ist für das Format und die Syntax der Konferenzbeschreibung unabhängig. Um bestimmte Aspekte der Konferenzbeschreibung zu bearbeiten, muss die Anwendung eine andere Schnittstelle Abfragen. Zurzeit werden nur SDP-Konferenz Beschreibungen unterstützt. die Anwendung muss **QueryInterface** für [**itsdp**](itsdp.md) verwenden, um auf die verschiedenen Felder der SDP-Konferenzbeschreibung zuzugreifen. Die **itconferenceblob** -Schnittstelle wird erstellt, indem **QueryInterface** für [**itdirectoryobject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject)aufgerufen wird.

## <a name="members"></a>Member

Die **itconferdenceblob** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Itconferenceblob** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **itconferenumceblob** -Schnittstelle verfügt über diese Methoden.



| Methode                                                             | BESCHREIBUNG                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_Zeichensatz erhalten**](itconferenceblob-get-characterset.md)     | Ruft den [**BLOB- \_ Zeichen \_ Satz**](blob-character-set.md) Indikator ab, der anzeigt, ob BLOB-Zeichen in ASCII, Unicode usw. enthalten sind.<br/> |
| [**get- \_ Konferenz-BLOB**](itconferenceblob-get-conferenceblob.md) | Ruft einen Zeiger auf das Konferenz-BLOB ab.<br/>                                                                                             |
| [**Init**](itconferenceblob-init.md)                              | Initialisiert das Konferenz-BLOB.<br/>                                                                                                   |
| [**Setconfererceblob**](itconferenceblob-setconferenceblob.md)    | Führt einen Commit für Änderungen am Konferenz-BLOB aus.<br/>                                                                                            |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI-Version<br/> | Erfordert TAPI 3,0 oder höher<br/>                                                 |
| Header<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Bibliothek<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

