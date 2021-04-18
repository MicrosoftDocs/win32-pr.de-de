---
description: Legt einen booleschen Wert fest, der angibt, ob Benutzeroberflächen Aufforderungen für die Identität eines Signatur Gebers oder Absenders verwendet werden können, oder ruft ihn ab.
ms.assetid: b9765de4-0b94-4006-aaa8-9ad6858da1f4
title: Settings. enablepromptforcertifiereui (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Settings.EnablePromptForCertificateUI
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: e494c98e2a828b512b0bb66dc2a44cba8c37792c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368597"
---
# <a name="settingsenablepromptforcertificateui-property"></a>Settings. enablepromptforcertifiereui (Eigenschaft)

\[Die **enablepromptforcertifi-EUI** -Eigenschaft ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind.\]

Mit der **enablepromptforcertifitoreui** -Eigenschaft wird ein boolescher Wert festgelegt oder abgerufen, der angibt, ob Benutzeroberflächen Aufforderungen für die Identität eines Signatur Gebers oder Absenders verwendet werden können.

## <a name="syntax"></a>Syntax


```VB
Settings.EnablePromptForCertificateUI As Boolean
```



## <a name="property-value"></a>Eigenschaftswert

**True** gibt an, dass die Benutzeroberfläche zur Eingabe eines Signatur Gebers oder der Absender Identität verwendet werden kann. Der Standardwert ist **false**.

> [!Note]  
> Wenn Sie diese Eigenschaft festlegen, werden Warnungen nicht deaktiviert, die generiert werden, bevor die Verwendung von privaten Schlüsseln aus einer webbasierten Anwendung erfolgt.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|----------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | CAPICOM 2,0 oder höher unter Windows Server 2003 und Windows XP<br/>                  |
| DLL<br/>             | <dl> <dt>Capicom.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Einstellungen**](settings.md)
</dt> </dl>

 

 




