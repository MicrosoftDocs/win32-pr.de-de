---
description: Die extractpatchxmldata-Methode des Installer-Objekts extrahiert Informationen aus einem Patch als XML-Zeichenfolge. Anhand dieser Informationen kann ermittelt werden, ob der Patch auf ein Zielsystem angewendet wird. Diese Methode ruft msiextractpatchxmldata auf.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Installer. extractpatchxmldata-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ExtractPatchXMLData
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 69c17236c0a4cd96820e0366df51b28cf47ecfb0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106367444"
---
# <a name="installerextractpatchxmldata-method"></a>Installer. extractpatchxmldata-Methode

Die **extractpatchxmldata** -Methode des [**Installer**](installer-object.md) -Objekts extrahiert Informationen aus einem Patch als XML-Zeichenfolge. Anhand dieser Informationen kann ermittelt werden, ob der Patch auf ein Zielsystem angewendet wird. Diese Methode ruft [**msiextractpatchxmldata**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)auf.

## <a name="syntax"></a>Syntax


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Patchpfad* 
</dt> <dd>

Vollständiger Pfad zum Patch, von dem die anwendbarkeits Informationen extrahiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer 3,0 oder höher unter Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msiextractpatchxmldata**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[Wird in Windows Installer 2,0 und früher nicht unterstützt.](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




