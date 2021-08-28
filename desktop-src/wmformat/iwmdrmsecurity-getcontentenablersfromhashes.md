---
title: IWMDRMSecurity GetContentEnablersFromHashes-Methode (Wmdrmsdk.h)
description: Die GetContentEnablersFromHashes-Methode ruft Schnittstellen für die Inhaltsermöglichung ab, die die Erneuerung von Komponenten basierend auf Hashzertifikaten ermöglichen.
ms.assetid: d7429859-b609-49a2-a369-d02260bc15bf
keywords:
- GetContentEnablersFromHashes-Methode windows Media Format
- GetContentEnablersFromHashes-Methode Windows Media Format, IWMDRMSecurity-Schnittstelle
- IWMDRMSecurity interface windows Media Format , GetContentEnablersFromHashes method
topic_type:
- apiref
api_name:
- IWMDRMSecurity.GetContentEnablersFromHashes
api_location:
- Wmdrmsdk.lib
- Wmdrmsdk.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d5b2b5e126555a0d09ea88017e2a290c180434b18fb8a61f668afd8e12fa02a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808550"
---
# <a name="iwmdrmsecuritygetcontentenablersfromhashes-method"></a>IWMDRMSecurity::GetContentEnablersFromHashes-Methode

Die **GetContentEnablersFromHashes-Methode** ruft Schnittstellen für die Inhaltsermöglichung ab, die die Erneuerung von Komponenten basierend auf Hashzertifikaten ermöglichen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetContentEnablersFromHashes(
  [in]      BSTR              *rgpbCertHashes,
  [in]      DWORD             cCerts,
  [in]      HRESULT           hResultHint,
  [out]     IMFContentEnabler **prgContentEnablers,
  [in, out] DWORD             *pcContentEnablers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*rgpbCertHashes* \[ In\]
</dt> <dd>

Array von Zertifikathashes zum Abrufen von Inhalts-Enablern.

</dd> <dt>

*cCerts* \[ In\]
</dt> <dd>

Anzahl der Zertifikate, für die Inhalts-Enabler abgerufen werden. Dies ist die Anzahl der Elemente im *rgpbCertHashes-Array.*

</dd> <dt>

*hResultHint* \[ In\]
</dt> <dd>

Gibt den Wert zurück, der von dem Vorgang empfangen wurde, der aufgrund eines gesperrten Zertifikats fehlgeschlagen ist. Wenn Sie nicht als Reaktion auf einen fehlgeschlagenen Methodenaufruf aufrufen, legen Sie auf S \_ OK fest.

</dd> <dt>

*prgContentEnablers* \[ out\]
</dt> <dd>

Array, das die Adressen der neu erstellten **BENUTZEROBERFLÄCHEContentEnabler-Schnittstellen** empfängt. Legen Sie diese **Option auf NULL** fest, um die Anzahl der Inhalts-Enabler im Parameter *pcContentEnablers* zu erhalten.

</dd> <dt>

*pcContentEnablers* \[ in, out\]
</dt> <dd>

Anzahl der Elemente im *prgContentEnablers-Array.* Wenn *prgContentEnablers* **NULL ist,** wird dieser Wert auf die Anzahl der erforderlichen Inhalts-Enabler in der Ausgabe festgelegt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Methode gibt ein **HRESULT** zurück. Mögliches Werte (aber nicht die Einzigen) sind die in der folgenden Tabelle.



| Rückgabecode                                                                          | Beschreibung                      |
|--------------------------------------------------------------------------------------|----------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl> | Die Methode wurde erfolgreich ausgeführt.<br/> |



 

## <a name="remarks"></a>Hinweise

Wenn Sie die **BENUTZEROBERFLÄCHEContentEnabler-Schnittstelle** verwenden, um gesperrte Komponenten zu erneuern, müssen Sie den Prozess für den Benutzer verdeutlichen. Diese Erläuterung muss getroffen werden, da der Updateprozess Informationen vom Clientcomputer an eine Microsoft-Website sendet.

Wenn Sie **DENTCONTENTEnabler::AutomaticEnable** aufrufen, startet die Inhalts-Aktivierung den Standardbrowser mit der Adresse des Updatediensts auf der Microsoft-Website. Ein eindeutiger Bezeichner, der die gesperrte Komponente identifiziert, wird an den Updatedienst gesendet. Der Dienst leitet den Browser dann zu einer Webseite um, von der der Benutzer möglicherweise die neue Version der gesperrten Komponente herunterladen und installieren kann.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Wmdrmsdk.h</dt> </dl>   |
| Bibliothek<br/> | <dl> <dt>Wmdrmsdk.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMDRMSecurity-Schnittstelle**](iwmdrmsecurity.md)
</dt> </dl>

 

 





