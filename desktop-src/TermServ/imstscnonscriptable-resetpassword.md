---
title: Imstscnonscriptable ResetPassword-Methode
description: Setzt alle Kenn Wort Zustände im Remotedesktop ActiveX-Steuerelement zurück.
ms.assetid: 889c4d41-fadf-4a5c-b4a8-0b349fd6db54
ms.tgt_platform: multiple
keywords:
- ResetPassword-Methode Remotedesktopdienste
- ResetPassword-Methode Remotedesktopdienste, imstscnonscriptable-Schnittstelle
- Imstscnonscriptable-Schnittstelle Remotedesktopdienste, ResetPassword-Methode
topic_type:
- apiref
api_name:
- IMsTscNonScriptable.ResetPassword
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0401b97d1b16fda97ba706aef5b795b9f9bc0f3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478882"
---
# <a name="imstscnonscriptableresetpassword-method"></a>Imstscnonscriptable:: ResetPassword-Methode

Setzt alle Kenn Wort Zustände im Remotedesktop ActiveX-Steuerelement zurück. Sie können diese Methode aufrufen, um Kenn Wörter zu löschen, die in einem der drei unterstützten Formate gespeichert sind: Klartext, portabel codiert oder Binär (nicht portabel) codiert. Beachten Sie, dass codierte Kenn Wörter nicht als sicher verschlüsselt angesehen werden sollten.

## <a name="syntax"></a>Syntax


```C++
HRESULT ResetPassword();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Gibt **\_ OK** zurück, wenn erfolgreich.

## <a name="remarks"></a>Bemerkungen

Sie können diese Methode zum Zurücksetzen des Kennworts für das Steuerelement nach dem Trennen der Verbindung abrufen. Dadurch wird sichergestellt, dass nachfolgende Verbindungen, die dieselbe Instanz des Steuer Elements verwenden, sich nicht automatisch mit einem zuvor festgelegten Kennwort anmelden.

Diese Methode kann nur aufgerufen werden, wenn sich das Remotedesktop ActiveX-Steuerelement nicht im verbundenen Zustand befindet. Diese Methode gibt **E \_ Fail** zurück, wenn Sie aufgerufen wird, wenn das Steuerelement verbunden ist. Um den verbundenen Status zu überprüfen, müssen Sie die [**get \_ Connected**](imstscax-connected.md) -Methode über die [**imstscax**](imstscax-interface.md) -Schnittstelle oder eine der Schnittstellen, die von ihr erbt, abrufen.

Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                               |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                         |
| Typbibliothek<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ imstscnonscriptable ist als c1e6743a-41c1-4a74-832a-0dd06c1c7a0e definiert.<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imstscnonscriptable**](imstscnonscriptable-interface.md)
</dt> </dl>

 

 





