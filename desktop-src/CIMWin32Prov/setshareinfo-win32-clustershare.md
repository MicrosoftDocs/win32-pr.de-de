---
description: Legt die Parameter der freigegebenen Ressource fest.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: Setshareingefo-Methode der Win32_ClusterShare-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.SetShareInfo
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: bda6fe36d1168045ea9f8d331ff334920ed1dd19
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106346037"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a>Setshareingefo-Methode der Win32 \_ clustershare-Klasse

Legt die Parameter der freigegebenen Ressource fest.

## <a name="syntax"></a>Syntax


```mof
uint32 SetShareInfo(
  [in, optional] uint32                   MaximumAllowed,
  [in, optional] string                   Description,
  [in, optional] Win32_SecurityDescriptor Access
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*MaximumAllowed* \[ in, optional\]
</dt> <dd>

Limit für die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.

</dd> <dt>

*Beschreibung* \[ in, optional\]
</dt> <dd>

Beschreibt die freigegebene Ressource.

</dd> <dt>

*Zugriff* \[ in, optional\]
</dt> <dd>

Sicherheits Beschreibung für Berechtigungen auf Benutzerebene. Eine Sicherheits Beschreibung enthält Informationen zu den Berechtigungen, den Besitzern und den Zugriffs Funktionen der Ressource. Weitere Informationen finden Sie unter [**Win32 \_ securityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

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

 

