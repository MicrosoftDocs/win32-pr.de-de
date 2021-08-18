---
description: Legt die Parameter der freigegebenen Ressource fest.
ms.assetid: 592d0fa6-c865-4f70-89c3-b58204a8c5a6
ms.tgt_platform: multiple
title: SetShareInfo-Methode der Win32_ClusterShare-Klasse
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
ms.openlocfilehash: 07245e97e091f607d142de57c00109d3671bd81b5f34b9062681229090ff6b50
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119439400"
---
# <a name="setshareinfo-method-of-the-win32_clustershare-class"></a>SetShareInfo-Methode der Win32 \_ ClusterShare-Klasse

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

Begrenzen Sie die maximale Anzahl von Benutzern, die diese Ressource gleichzeitig verwenden dürfen.

</dd> <dt>

*Beschreibung* \[ in, optional\]
</dt> <dd>

Beschreibt die Ressource, die freigegeben wird.

</dd> <dt>

*Zugriff* \[ in, optional\]
</dt> <dd>

Sicherheitsbeschreibung für Berechtigungen auf Benutzerebene. Eine Sicherheitsbeschreibung enthält Informationen über die Berechtigungs-, Besitzer- und Zugriffsfunktionen der Ressource. Weitere Informationen finden Sie unter [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7<br/>                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008 R2<br/>                                                       |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**Win32 \_ ClusterShare**](win32-clustershare.md)
</dt> </dl>

 

