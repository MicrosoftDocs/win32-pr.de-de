---
description: Legt den Titel und Untertitel fest, die im Assistentenheader angezeigt werden. Im Allgemeinen zeigt der Client den Header über dem HTML-Code und unterhalb der Titelleiste an.
title: WebWizardHost.SetHeaderText-Methode (Shldisp.h)
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
ms.openlocfilehash: d97bb8ac1823801257f0ad9f2a737a78bafbf6d724c0f56f3ff0607e498a61bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859194"
---
# <a name="webwizardhostsetheadertext-method"></a>WebWizardHost.SetHeaderText-Methode

Legt den Titel und Untertitel fest, die im Assistentenheader angezeigt werden. Im Allgemeinen zeigt der Client den Header über dem HTML-Code und unterhalb der Titelleiste an.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrHeaderTitle* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine Zeichenfolge, die den Titel enthält.

</dd> <dt>

*bstrHeaderSubtitle* \[ In\]
</dt> <dd>

Typ: **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Eine Zeichenfolge, die den Untertitel enthält.

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 
