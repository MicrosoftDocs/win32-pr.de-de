---
description: Aktualisiert die Schaltflächen Zurück, Weiter und Fertig stellen im Assistentenframe des Clients.
title: WebWizardHost.SetWizardButtons-Methode (Shldisp.h)
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
ms.openlocfilehash: a1b2a79c7ea323c36371e08d3519e71e4c537935
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842621"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>WebWizardHost.SetWizardButtons-Methode

Aktualisiert die Schaltflächen **Zurück,** **Weiter** und **Fertig stellen** im Assistentenframe des Clients.

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

*vbEnableBack* \[ In\]
</dt> <dd>

Typ: **Boolean**

Aktiviert die Schaltfläche **Zurück.**

</dd> <dt>

*vbEnableNext* \[ In\]
</dt> <dd>

Typ: **Boolescher Wert**

Hiermit wird die Schaltfläche **Weiter** aktiviert.

</dd> <dt>

*vbLastPage* \[ In\]
</dt> <dd>

Typ: **Boolescher Wert**

Aktiviert die Schaltfläche **Fertig stellen.** Gibt an, dass dies die letzte serverseitige Seite ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Stellen Sie sicher, dass Sie Handlerfunktionen auf jeder serverseitigen Seite für OnBack() und OnNext() implementieren, die den Assistentenschaltflächen **Zurück** und **Weiter** entsprechen. Die Funktionen OnBack() und OnNext() reagieren auf **SetWizardButtons**. Zur entsprechenden Zeit ruft die OnNext()-Funktion **SetWizardButtons** mit *vbLastPage* = **true** auf, wodurch eine **Fertig stellen-Schaltfläche** aktiviert werden kann. OnNext() ruft auch [**FinalNext**](iwebwizardhost-finalnext.md) auf, wenn ein Benutzer auf die Schaltfläche **Fertig stellen** klickt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




