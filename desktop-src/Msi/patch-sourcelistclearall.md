---
description: Die SourceListClearAll-Methode des Patch-Objekts löscht die vollständige Quellliste aller Quellen des angegebenen Typs für einen Patch. Akzeptiert Type als Parameter. Diese Methode ruft MsiSourceListClearAllEx auf.
ms.assetid: 9458a3db-8eaa-4067-875f-8fac68bdf1f8
title: Patch.SourceListClearAll-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearAll
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ae7de8c0a830000b3100e84cacbf088fefb592ddaa912a7737a35ea009a3cfe1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942300"
---
# <a name="patchsourcelistclearall-method"></a>Patch.SourceListClearAll-Methode

Die **SourceListClearAll-Methode** des [**Patch-Objekts**](patch-object.md) löscht die vollständige Quellliste aller Quellen des angegebenen Typs für einen Patch. Akzeptiert *Type* als Parameter. Diese Methode ruft [**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)auf.

## <a name="syntax"></a>Syntax


```JScript
Patch.SourceListClearAll(
  Type
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* 
</dt> <dd>

Der Typ des Quelltyps, z. B. Netzwerk, URL oder Medien.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IPatch ist als 000C10A1-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearAllEx**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearallexa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




