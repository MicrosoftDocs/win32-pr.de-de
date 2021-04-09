---
description: Gibt eine UInt32-Bitmap mit den Zugriffsrechten für die Freigabe zurück, die der Benutzer oder die Gruppe hat, in deren Auftrag die Instanz zurückgegeben wird.
ms.assetid: 1f656c63-f5ee-4b14-845a-0eb34a0e7a64
ms.tgt_platform: multiple
title: Getaccessmask-Methode der Win32_ClusterShare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: db27998c362e3df350dd12b6b91f3966cfc152ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104126512"
---
# <a name="getaccessmask-method-of-the-win32_clustershare-class"></a>Getaccessmask-Methode der Win32 \_ clustershare-Klasse

Gibt eine **UInt32** -Bitmap mit den Zugriffsrechten für die Freigabe zurück, die der Benutzer oder die Gruppe hat, in deren Auftrag die Instanz zurückgegeben wird.

## <a name="syntax"></a>Syntax


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Zugriffsrechte für die Freigabe, die der Benutzer oder die Gruppe innehat.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | Root \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Win32- \_ clustershare**](win32-clustershare.md)
</dt> </dl>

 

 




