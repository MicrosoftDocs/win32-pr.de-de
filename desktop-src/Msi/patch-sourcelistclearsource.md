---
description: Entfernt eine Netzwerk-oder URL-Quelle.
ms.assetid: 76c7cc6c-740f-40e0-8385-024dcc82b79e
title: Patch. sourcelistclearsource-Methode
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
ms.openlocfilehash: 7a85afc4eb85a4269284a49809c399dbb65b4894
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106351229"
---
# <a name="patchsourcelistclearsource-method"></a>Patch. sourcelistclearsource-Methode

Die **sourcelistclearsource** -Methode entfernt eine Netzwerk-oder URL-Quelle. Diese Methode ruft [**msisourcelistclearsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)auf.

## <a name="syntax"></a>Syntax


```JScript
Patch.SourceListClearSource(
  Type,
  SourcePath
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Type* 
</dt> <dd>

Der Typ der Quelle, die entfernt werden soll.

<dl><span id="MSISOURCETYPE_NETWORK"></span><span id="msisourcetype_network"></span><dt>

**msisourcetype- \_ Netzwerk**
</dt><span id="MSISOURCETYPE_URL"></span><span id="msisourcetype_url"></span><dt>

**msisourcetype- \_ URL**
</dt> </dl> </dd> <dt>

*SourcePath* 
</dt> <dd>

Der Pfad zur Quelle, die entfernt werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003, Windows XP und Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ iPatch ist definiert als 000c10a1-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                            |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Patch**](patch-object.md)
</dt> <dt>

[**Msisourcelistclearsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistclearsourcea)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




