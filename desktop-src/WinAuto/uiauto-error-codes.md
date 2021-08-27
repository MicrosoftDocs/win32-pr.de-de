---
title: Fehlercodes (UIAutomationCoreApi.h)
description: In diesem Thema werden die Fehlercodes beschrieben, die von Microsoft Benutzeroberflächenautomatisierung.
ms.assetid: f7820aa3-908e-426e-851c-84397019d735
topic_type:
- apiref
api_name:
- UIA_E_ELEMENTNOTAVAILABLE
- UIA_E_ELEMENTNOTENABLED
- UIA_E_INVALIDOPERATION
- UIA_E_NOCLICKABLEPOINT
- UIA_E_NOTSUPPORTED
- UIA_E_PROXYASSEMBLYNOTLOADED
- UIA_E_TIMEOUT
api_location:
- UIAutomationCoreApi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc0e2e9e100c8beb76b96fea85d999ed78102ff33b9827f36fc745270f0286f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118827342"
---
# <a name="error-codes-uiautomationcoreapih"></a>Fehlercodes (UIAutomationCoreApi.h)

In diesem Thema werden die Fehlercodes beschrieben, die von Microsoft Benutzeroberflächenautomatisierung. Die Liste ist alphabetisch nach Namen sortiert.



| Konstante/Wert                                                                                                                                                                                                                                                              | Beschreibung                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <dt>**UIA \_ E \_ ELEMENTNOTAVAILABLE**</dt> <dt>0x80040201</dt> </dl>          | Gibt an, dass eine Methode für ein virtualisiertes Element oder für ein Element aufgerufen wurde, das nicht mehr vorhanden ist, in der Regel, weil es zerstört wurde. <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <dt>**UIA \_ E \_ ELEMENTNOTENABLED**</dt> <dt>0x80040200</dt> </dl>                | Gibt an, dass eine Methode, die ein aktiviertes Element erfordert, z. B. [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) oder [**Expand,**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)für ein deaktiviertes Element aufgerufen wurde. <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <dt>**UIA \_ E \_ INVALIDOPERATION-0x80131509**</dt> <dt></dt> </dl>                   | Gibt an, dass die -Methode versucht hat, einen ungültigen Vorgang zu versuchen.<br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <dt>**UIA \_ E \_ NOCLICKABLEPOINT-0x80040202**</dt> <dt></dt> </dl>                   | Gibt an, dass [**die GetClickablePoint-Methode**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) für ein Element aufgerufen wurde, das keinen klickbaren Punkt hat.<br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <dt>**UIA \_ E \_ NOTSUPPORTED**</dt> <dt>0x80040204</dt> </dl>                               | Gibt an, dass der Anbieter die angegebene Eigenschaft oder das angegebene Steuerelementmuster explizit nicht unterstützt. Benutzeroberflächenautomatisierung gibt diesen Fehlercode an den Aufrufer zurück, ohne einen Standardwert bereitstellen oder auf einen anderen Anbieter zurückfallen zu müssen.<br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <dt>**UIA \_ E \_ PROXYASSEMBLYNOTLOADED**</dt> <dt>0x80040203</dt> </dl> | Gibt an, dass beim Laden einer Assembly, die einen clientseitigen Anbieter (Proxy) enthält, ein Problem aufgetreten ist.<br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <dt>**UIA \_ E \_ TIMEOUT-0x80131505**</dt> <dt></dt> </dl>                                                      | Gibt an, dass die für einen Prozess oder Vorgang zugewiesene Zeit abgelaufen ist.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                             |
| Header<br/>                   | <dl> <dt>UIAutomationCoreApi.h</dt> </dl> |



 

 





