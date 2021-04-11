---
title: Inapcomponentconfig invokeui-Methode (napcommon. h)
description: Hiermit wird eine angepasste Benutzeroberfläche für eine Komponente der System Integritätsprüfung (System Health Prüfungs, SHV) gestartet
ms.assetid: da2a5e3e-bc17-4984-bdbe-b72e9e710a9d
keywords:
- Invokeui-Methode NAP
- Invokeui-Methode NAP, inapcomponentconfig-Schnittstelle
- Inapcomponentconfig-Schnittstelle NAP, invokeui-Methode
topic_type:
- apiref
api_name:
- INapComponentConfig.InvokeUI
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dd86d683365286fc2130c1ac9edf21ff075d61a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949674"
---
# <a name="inapcomponentconfiginvokeui-method"></a>Inapcomponentconfig:: invokeui-Methode

> [!Note]  
> Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.

 

Die **invokeui** -Methode gestartet eine angepasste Benutzeroberfläche für eine Komponente der System Integritätsprüfung (System Health Prüfungs, SHV).

## <a name="syntax"></a>Syntax


```C++
HRESULT InvokeUI(
  [in] HWND hwndParent
) const;
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hwndParent* \[ in\]
</dt> <dd>

Ein Handle für das übergeordnete Fenster oder Besitzer Fenster. Ein gültiges Fenster Handle muss angegeben werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt basierend auf dem Ergebnis dieses Vorgangs einen der folgenden Fehlercodes zurück.



| Rückgabecode                                                                                     | Beschreibung                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>           | Der Vorgang ist erfolgreich.<br/>                            |
| <dl> <dt>**E \_ Access verweigert**</dt> </dl> | Berechtigungs Fehler, Zugriff verweigert.<br/>                       |
| <dl> <dt>**E \_ Outo-Memory**</dt> </dl>  | System Ressourcen Limit, der Vorgang konnte nicht durchgeführt werden.<br/> |
| <dl> <dt>**E \_ notimpl**</dt> </dl>       | Der SHV unterstützt keine angepasste Benutzeroberfläche.<br/>               |



 

## <a name="remarks"></a>Bemerkungen

Dieser Methodenaufrufe sollte blockieren, bis die SHV-Benutzeroberfläche beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nicht unterstützt<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Napcommon. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Napcommon. idl</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Inapcomponentconfig**](inapcomponentconfig.md)
</dt> <dt>

[**Inapcomponentconfig:: isuisupported**](inapcomponentconfig-isuisupported.md)
</dt> </dl>

 

 





