---
description: Legt den Titel und den Untertitel fest, die im Assistenten Header angezeigt werden. Im Allgemeinen zeigt der Client den Header oberhalb von HTML und unterhalb der Titelleiste an.
title: Webwizardhost. abadertext-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: 92e23fab94cfedd8bbc62e31086759af48238a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980256"
---
# <a name="webwizardhostsetheadertext-method"></a>Webwizardhost. abadertext-Methode

Legt den Titel und den Untertitel fest, die im Assistenten Header angezeigt werden. Im Allgemeinen zeigt der Client den Header oberhalb von HTML und unterhalb der Titelleiste an.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrinheadertitle* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Zeichenfolge, die den Titel enthält.

</dd> <dt>

*bstrinheaderuntertitel* \[ in\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Zeichenfolge, die Untertitel enthält.

</dd> </dl>

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 
