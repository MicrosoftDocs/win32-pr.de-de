---
title: Iwmpcdromburn-aktuasestatus-Methode
description: Die Aktualisierungs Status-Methode aktualisiert die Statusinformationen für die aktuelle Burn-Wiedergabeliste.
ms.assetid: 4dd90e76-92b5-4a00-b027-b54502e56804
keywords:
- aktuasestatusmethode Windows Media Player
- aktuasestatusmethode Windows Media Player, iwmpcdromburn-Schnittstelle
- Iwmpcdromburn Interface, Windows Media Player, aktuaktuasestatusmethode
topic_type:
- apiref
api_name:
- IWMPCdromBurn.refreshStatus
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55205e684d055d20c8e8f218ba58716de8472916
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364778"
---
# <a name="iwmpcdromburnrefreshstatus-method"></a>Iwmpcdromburn:: erfrischendes Status-Methode

Die Aktualisierungs **Status** -Methode aktualisiert die Statusinformationen für die aktuelle Burn-Wiedergabeliste.

## <a name="syntax"></a>Syntax


```CSharp
public void refreshStatus();
```


```VB

Public Sub refreshStatus()
Implements IWMPCdromBurn.refreshStatus
```





## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Rufen Sie diese Methode auf, nachdem Sie eine Burn-Wiedergabeliste erstellt oder geändert haben, bevor Sie die Statusinformationen lesen oder die CD brennen. Sie können testen, ob eine Aktualisierung erforderlich ist, indem Sie den Wert von **burnstate** und die Überprüfung auf wmpbsrefresh statuausgaben durchsuchen.

Das Aktualisieren des Status ist ein synchroner Vorgang. Dies bedeutet, dass eine lange Zeitspanne vergehen kann, bevor diese Methode zurückgibt, wenn die aktuelle Burn-Wiedergabeliste groß ist und viele Änderungen enthält.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| Version<br/>   | Windows Media Player 11.<br/>                                                                                    |
| Namespace<br/> | **WMPLib**<br/>                                                                                                  |
| Assembly<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iwmpcdromburn-Schnittstelle (VB und c#)**](iwmpcdromburn--vb-and-c.md)
</dt> <dt>

[**Iwmpcdromburn. burnstate (VB und c#)**](wmplibiwmpcdromburn-iwmpcdromburn-burnstate--vb-and-c.md)
</dt> <dt>

[**Wmpburnstate**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate)
</dt> </dl>

 

 





