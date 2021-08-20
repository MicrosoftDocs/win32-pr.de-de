---
description: Entfernt ein Netzwerk oder eine URL-Quelle.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Patch.SourceListClearSource-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Patch.SourceListClearSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 75ffcf17329dfd3c8cc4a048035162658f9ccc0f5264805bb0ef8403082805a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118942270"
---
# <a name="patchsourcelistclearsource-method"></a>Patch.SourceListClearSource-Methode

Die **SourceListClearSource-Methode** entfernt ein Netzwerk oder eine URL-Quelle. Diese Methode ruft [**MsiSourceListClearSource auf.**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)

## <a name="syntax"></a>Syntax


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Typ* 
</dt> <dd>

Typ der zu entfernenden Quelle.

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

**MSISOURCETYPE \_ NETWORK**
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

**MSISOURCETYPE-URL \_**
</dt> </dl> </dd> <dt>

*Sourcepath* 
</dt> <dd>

Pfad zur zu entfernenden Quelle.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IPatch ist als \_ 000C10A1-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**MsiSourceListClearSource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




