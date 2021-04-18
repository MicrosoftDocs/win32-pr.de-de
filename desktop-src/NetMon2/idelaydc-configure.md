---
description: Die Configure-Methode übermittelt Konfigurationsinformationen, die für eine Erfassung verwendet werden.
ms.assetid: 6418c465-c339-44b6-84eb-36c7b89231f8
title: Idelta aydcconfigure-Methode (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDelaydC.Configure
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 0fa91c5b46d2eb7ca21ba14aa00b274d52e77eb1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484315"
---
# <a name="idelaydcconfigure-method"></a>Idelta aydc:: Configure-Methode

Die **configure** -Methode übermittelt Konfigurationsinformationen, die für eine Erfassung verwendet werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT STDMETHODCALLTYPE Configure(
  [in]  HBLOB hConfigurationBlob,
  [out] HBLOB hErrorBlob
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hconfigurationblob* \[ in\]
</dt> <dd>

Handle für das BLOB, das die Konfigurationsinformationen enthält.

</dd> <dt>

*herrorblob* \[ vorgenommen\]
</dt> <dd>

Handle für ein fehlerblob, das zusätzliche Fehlerinformationen enthält. Informationen zum Inhalt eines Fehler-BLOB finden Sie im Abschnitt "Hinweise" in diesem Thema.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn diese Methode erfolgreich ist, ist der Rückgabewert nmerr \_ Success.

Wenn die Methode nicht erfolgreich ist, ist der Rückgabewert einer der folgenden Fehlercodes:



| Rückgabecode                                                                                                      | Beschreibung                                                                               |
|------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**nmerr- \_ Erfassung**</dt> </dl>                  | Der NPP meldet, dass die Erfassungs Sitzung gestartet wurde.<br/>                          |
| <dl> <dt>**nmerr-Datenträger \_ \_ nicht \_ lokal \_ korrigiert**</dt> </dl>    |                                                                                           |
| <dl> <dt>**nmerr \_ konnte \_ keinen \_ Arbeits \_ Speicher erstellen.**</dt> </dl> |                                                                                           |
| <dl> <dt>**nicht genügend Arbeits \_ \_ Speicher für nmerr \_**</dt> </dl>            | Es war kein Arbeitsspeicher verfügbar. Fahren Sie Windows herunter, um Ressourcen freizugeben.<br/>               |
| <dl> <dt>**Ungültiger nmerr- \_ \_ Parameter**</dt> </dl>         | Das vom hconfiguration-Parameter angegebene konfigurationsblob ist ungültig.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Sie müssen diese Methode anwenden, um eine NPP neu zu starten, die gestartet, beendet, aber nicht getrennt wurde.

Der von *herrorblob* zurückgegebene fehlerblob enthält Einträge, die Netzwerkmonitor in dem in *hconfigurationblob* angegebenen Konfigurations-BLOB nicht verstehen oder finden konnten. Das zurückgegebene fehlerblob enthält Fehlerinformationen, die von der Anwendung für die Problembehandlung verwendet werden können. Wenn z. b. der nmerr- \_ \_ blobeintrag \_ \_ nicht \_ vorhanden ist, wird der Eintrag Netzwerkmonitor der nicht gefunden wurde, im zurückgegebenen fehlerblob enthalten ist.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                                                                     |
| Header<br/>                   | <dl> <dt>Netmon. h</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll; </dt> <dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Idelta-DC](idelaydc.md)
</dt> <dt>

[Idelta aydc:: Connect](idelaydc-connect.md)
</dt> <dt>

[Idelta aydc:: Start](idelaydc-start.md)
</dt> <dt>

[Idelta aydc:: Beendigung](idelaydc-stop.md)
</dt> </dl>

 

 




