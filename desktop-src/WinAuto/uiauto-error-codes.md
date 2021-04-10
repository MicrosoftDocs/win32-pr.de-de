---
title: Fehler Codes (uiautomationcoreapi. h)
description: In diesem Thema werden die von der Microsoft-Benutzeroberflächen Automatisierung verfügbar gemachten Fehlercodes beschrieben.
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
ms.openlocfilehash: baaa03746bfb1a5e56fcac8b39d326581159f459
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040032"
---
# <a name="error-codes-uiautomationcoreapih"></a>Fehler Codes (uiautomationcoreapi. h)

In diesem Thema werden die von der Microsoft-Benutzeroberflächen Automatisierung verfügbar gemachten Fehlercodes beschrieben. Die Liste wird alphabetisch nach dem Namen sortiert.



| Konstante/Wert                                                                                                                                                                                                                                                              | BESCHREIBUNG                                                                                                                                                                                                                                              |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="UIA_E_ELEMENTNOTAVAILABLE"></span><span id="uia_e_elementnotavailable"></span><dl> <dt>**UIA \_ E \_ elementnotavailable**</dt> <dt>0x80040201</dt> </dl>          | Gibt an, dass eine Methode für ein virtualisiertes Element oder für ein Element aufgerufen wurde, das nicht mehr vorhanden ist. Dies ist normalerweise darauf zurückzuführen, dass es zerstört wurde. <br/>                                                                                                  |
| <span id="UIA_E_ELEMENTNOTENABLED"></span><span id="uia_e_elementnotenabled"></span><dl> <dt>**UIA \_ E \_ elementnotenabled**</dt> <dt>0x80040200</dt> </dl>                | Gibt an, dass eine Methode, die ein aktiviertes Element benötigt (z. b. [**Select**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iselectionitemprovider-select) oder [**Expand**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-iexpandcollapseprovider-expand)), für ein Element aufgerufen wurde, das deaktiviert wurde. <br/>             |
| <span id="UIA_E_INVALIDOPERATION"></span><span id="uia_e_invalidoperation"></span><dl> <dt>**UIA \_ E \_ InvalidOperation**</dt> <dt>0x80131509</dt> </dl>                   | Gibt an, dass die Methode einen ungültigen Vorgang versucht hat.<br/>                                                                                                                                                                          |
| <span id="UIA_E_NOCLICKABLEPOINT"></span><span id="uia_e_noclickablepoint"></span><dl> <dt>**UIA \_ E \_ noclickablepoint**</dt> <dt>0x80040202</dt> </dl>                   | Gibt an, dass die [**GetClickablePoint**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationelement-getclickablepoint) -Methode für ein Element aufgerufen wurde, das über keinen durch Klicken aktivierbaren Punkt verfügt.<br/>                                                                                    |
| <span id="UIA_E_NOTSUPPORTED"></span><span id="uia_e_notsupported"></span><dl> <dt>**UIA \_ E \_ NotSupported**</dt> <dt>0x80040204</dt> </dl>                               | Gibt an, dass der Anbieter die angegebene Eigenschaft oder das angegebene Steuerelement Muster explizit nicht unterstützt. Die Benutzeroberflächen Automatisierung gibt diesen Fehlercode an den Aufrufer zurück, ohne zu versuchen, einen Standardwert anzugeben oder auf einen anderen Anbieter zurückzukehren.<br/> |
| <span id="UIA_E_PROXYASSEMBLYNOTLOADED"></span><span id="uia_e_proxyassemblynotloaded"></span><dl> <dt>**UIA \_ E \_ proxyassemblynotloaded**</dt> <dt>0x80040203</dt> </dl> | Gibt an, dass beim Laden einer Assembly, die einen Client seitigen (Proxy-) Anbieter enthält, ein Problem aufgetreten ist.<br/>                                                                                                                                      |
| <span id="UIA_E_TIMEOUT"></span><span id="uia_e_timeout"></span><dl> <dt>**UIA \_ E \_ Timeout**</dt> <dt>0x80131505</dt> </dl>                                                      | Gibt an, dass die für einen Prozess oder einen Vorgang vorgesehene Zeit abgelaufen ist.<br/>                                                                                                                                                                      |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                             |
| Header<br/>                   | <dl> <dt>Uiautomationcoreapi. h</dt> </dl> |



 

 





