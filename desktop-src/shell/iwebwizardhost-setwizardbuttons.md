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
ms.openlocfilehash: 36b40d0831c18a7931f3f29492dd4c7769440a76ddcec2aa33ba3e840e97950d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859123"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>WebWizardHost.SetWizardButtons-Methode

Aktualisiert die **Schaltflächen Zurück,** **Weiter** und **Fertig stellen** im Assistentenframe des Clients.

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

Typ: **Boolesch**

Aktiviert die Schaltfläche **Zurück.**

</dd> <dt>

*vbEnableNext* \[ In\]
</dt> <dd>

Typ: **Boolesch**

Hiermit wird die Schaltfläche **Weiter** aktiviert.

</dd> <dt>

*vbLastPage* \[ In\]
</dt> <dd>

Typ: **Boolesch**

Aktiviert die Schaltfläche **Fertig** stellen. Gibt an, dass dies die letzte serverseitige Seite ist.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Achten Sie darauf, handler-Funktionen auf jeder serverseitigen Seite für OnBack() und OnNext() zu implementieren, die den Assistentenschaltflächen **Zurück** und **Weiter entspricht.** Die Funktionen OnBack() und OnNext() reagieren auf **SetWizardButtons.** Zum entsprechenden Zeitpunkt ruft die OnNext()-Funktion **SetWizardButtons** mit *vbLastPage* true auf, wodurch die Schaltfläche = Fertig stellen **aktiviert werden** kann. OnNext() ruft auch [**FinalNext**](iwebwizardhost-finalnext.md) auf, wenn ein Benutzer auf die Schaltfläche **Fertig stellen** klickt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Shldisp.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Shldisp.idl</dt> </dl> |



 

 




