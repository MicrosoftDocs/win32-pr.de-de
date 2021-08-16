---
description: Erstellt die angegebene Schnittstelle.
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: ISCardManage::CreateInterface-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8c9b231ec7930b78c1693e38268638e7a24b26dfa32d8f25acb5a429dbcdedc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922659"
---
# <a name="iscardmanagecreateinterface-method"></a>ISCardManage::CreateInterface-Methode

\[Die **CreateInterface-Methode** ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt Anforderungen angegeben sind. Die [Smartcardmodule](/previous-versions/windows/desktop/secsmart/smart-card-modules) bieten ähnliche Funktionen.\]

Die **CreateInterface-Methode** erstellt die angegebene Schnittstelle.

## <a name="syntax"></a>Syntax


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguidInterface* \[ In\]
</dt> <dd>

Der GUID-Wert der zu erstellende Schnittstelle.

</dd> <dt>

*bstrName* \[ In\]
</dt> <dd>

Der Name der Schnittstelle, die erstellt werden soll, wenn die GUID nicht verfügbar ist. Standardwerte sind "CryptoProvider".

</dd> <dt>

*pUserData* \[ In\]
</dt> <dd>

Zeiger auf benutzerspezifische Daten, die bei der Erstellung einer Schnittstelle verwendet werden sollen.

</dd> <dt>

*ppInterface* \[ out\]
</dt> <dd>

Zeiger auf die zurückgegebene Schnittstelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Folgende Rückgabewerte sind möglich:



| Rückgabecode                                                                                   | Beschreibung                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operation erfolgreich abgeschlossen.<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Einer der angegebenen Parameter ist ungültig.<br/>                                         |
| <dl> <dt>**E \_ POINTER**</dt> </dl>     | Ein ungültiger Zeiger wurde entweder im *pguidInterface-* oder im *pUserData-Parameter* übergeben.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Nicht genügend Arbeitsspeicher.<br/>                                                                        |



 

## <a name="remarks"></a>Hinweise

Eine Liste aller von der [**ISCardManage-Schnittstelle**](iscardmanage.md) definierten Methoden finden Sie unter **ISCardManage.**

Zusätzlich zu den oben aufgeführten COM-Fehlercodes kann diese Schnittstelle einen [*Smartcardfehlercode*](../secgloss/s-gly.md) zurückgeben, wenn eine Smartcardfunktion aufgerufen wurde, um die Anforderung abzuschließen. Informationen zu Smartcard-Fehlercodes finden Sie unter [Smartcard-Rückgabewerte.](authentication-return-values.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>          |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/> |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
