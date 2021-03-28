---
description: Aktualisiert die Schaltflächen zurück, weiter und Fertigstellen im Assistenten Rahmen des Clients.
title: Webwizardhost. * twizardbuttons-Methode (Shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980249"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>Webwizardhost. * twizardbuttons-Methode

Aktualisiert die Schaltflächen **zurück**, **weiter** und **Fertig** stellen im Assistenten Rahmen des Clients.

## <a name="syntax"></a>Syntax


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*vbenableback* \[ in\]
</dt> <dd>

Typ: **Boolean**

Aktiviert die Schaltfläche " **zurück** ".

</dd> <dt>

*vbenablenext* \[ in\]
</dt> <dd>

Typ: **Boolean**

Hiermit wird die Schaltfläche **Weiter** aktiviert.

</dd> <dt>

*vblastpage* \[ in\]
</dt> <dd>

Typ: **Boolean**

Aktiviert die Schaltfläche **Fertig** stellen. Gibt an, dass dies die letzte serverseitige Seite ist.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Stellen Sie sicher, dass Sie Handlerfunktionen auf jeder serverseitigen Seite für onback () und OnNext () implementieren, die den Assistenten-Schaltflächen **zurück** und **weiter** entspricht. Die onback ()-Funktion und die OnNext ()-Funktion Antworten auf " **".** Zum entsprechenden **Zeitpunkt Ruft die** OnNext ()-Funktion "" mit " *vblastpage* = **true**" auf, wodurch eine Schaltfläche **Fertig** stellen aktiviert werden kann. OnNext () ruft auch [**finalnext**](iwebwizardhost-finalnext.md) auf, wenn ein Benutzer auf die Schaltfläche **Fertig** stellen klickt.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




