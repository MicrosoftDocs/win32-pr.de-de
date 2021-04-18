---
title: IWMPSettings2 mediaaccessrights (Eigenschaft)
description: Die mediaaccessrights-Eigenschaft ruft einen Wert ab, der die Berechtigungen angibt, die derzeit für den Bibliotheks Zugriff erteilt werden
ms.assetid: c4289a2c-e343-405d-9bf5-0e97f6617916
keywords:
- Media Access Rights-Eigenschaften Fenster Media Player
- mediaaccessrights-Eigenschaft, Windows Media Player, IWMPSettings2-Schnittstelle
- IWMPSettings2 Interface Windows Media Player, mediaaccessrights-Eigenschaft
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
ms.openlocfilehash: 96cca06b9618767e7748b4b1308ed97860c7c80b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354435"
---
# <a name="iwmpsettings2mediaaccessrights-property"></a>IWMPSettings2:: mediaaccessrights (Eigenschaft)

Die **mediaaccessrights** -Eigenschaft ruft einen Wert ab, der die Berechtigungen angibt, die derzeit für den Bibliotheks Zugriff erteilt werden

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```CSharp
public System.String mediaAccessRights {get;}
```


```VB

Public ReadOnly Property mediaAccessRights As System.String
```





## <a name="property-value"></a>Eigenschaftswert

Ein **System. String** -Wert, der einem der folgenden Werte entspricht.



| Wert | BESCHREIBUNG                      |
|-------|----------------------------------|
| none  | Nur die aktuellen Element Zugriffsrechte. |
| Lesen  | Nur Lese Zugriffsrechte.         |
| Voll  | Lese-/Schreibzugriffsrechte.        |



 

## <a name="remarks"></a>Bemerkungen

Eine Webseite muss zuerst die Berechtigung des Benutzers anfordern, Informationen aus der Bibliothek zu lesen oder Daten in die Bibliothek zu schreiben. Dies bedeutet, dass auf bestimmte Methoden, Eigenschaften und Ereignisse von Code aus nicht zugegriffen werden kann, wenn die entsprechenden Zugriffsrechte nicht erteilt wurden. Zum Abrufen von Zugriffsrechten Ruft die Anwendung **IWMPSettings2. get \_ requestmediaaccessrights** auf und übergibt einen Parameter, der die gewünschte Zugriffsrechte Ebene angibt.

Anwendungen, die auf dem Computer des Benutzers ausgeführt werden, haben immer vollständige Zugriffsrechte.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 9-Serie oder höher<br/>                                                                      |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IWMPSettings2-Schnittstelle (VB und c#)**](iwmpsettings2--vb-and-c.md)
</dt> <dt>

[**IWMPSettings2. requestmediaaccessrights (VB und c#)**](wmplibiwmpsettings2-iwmpsettings2-requestmediaaccessrights--vb-and-c.md)
</dt> </dl>

 

 





