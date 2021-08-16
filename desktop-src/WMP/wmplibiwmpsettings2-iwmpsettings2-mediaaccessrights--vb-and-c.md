---
title: IWMPSettings2 mediaAccessRights-Eigenschaft
description: Die mediaAccessRights-Eigenschaft ruft einen Wert ab, der die derzeit für den Bibliothekszugriff gewährten Berechtigungen angibt.
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- mediaAccessRights-Eigenschaft Windows Media Player
- mediaAccessRights-Eigenschaft Windows Media Player , IWMPSettings2-Schnittstelle
- IWMPSettings2-Schnittstelle Windows Media Player , mediaAccessRights-Eigenschaft
topic_type:
- apiref
api_name:
- IWMPSettings2.mediaAccessRights
- IWMPSettings2.get_mediaAccessRights
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 797e45c62b505033afd2126f79d5830de5bc9847a4de36199a6c919a4978f112
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120122490"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a>IWMPSettings2::mediaAccessRights-Eigenschaft

Die **mediaAccessRights-Eigenschaft** ruft einen Wert ab, der die derzeit für den Bibliothekszugriff gewährten Berechtigungen angibt.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Eine **System.String,die** einer der folgenden Werte ist.



| Wert | BESCHREIBUNG                      |
|-------|----------------------------------|
| Keine  | Nur aktuelle Elementzugriffsrechte. |
| Lesen  | Nur Lesezugriffsrechte.         |
| Voll  | Lese-/Schreibzugriffsrechte.        |



 

## <a name="remarks"></a>Hinweise

Eine Webseite muss zunächst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben. Dies bedeutet, dass der Code auf bestimmte Methoden, Eigenschaften und Ereignisse nicht zugreifen kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden. Um Zugriffsrechte zu erhalten, ruft die Anwendung **IWMPSettings2.get \_ requestMediaAccessRights** auf und übergibt einen Parameter, der die gewünschte Zugriffsrechteebene angibt.

Anwendungen, die auf dem Computer des Benutzers ausgeführt werden, verfügen immer über Vollzugriffsrechte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9er Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IWMPSettings2-Schnittstelle (VB und C#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2.requestMediaAccessRights (VB und C#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





