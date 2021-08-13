---
description: Die ExtractPatchXMLData-Methode des Installer-Objekts extrahiert Informationen aus einem Patch als XML-Zeichenfolge. Die Informationen können verwendet werden, um zu bestimmen, ob der Patch auf einem Zielsystem angewendet wird. Diese Methode ruft MsiExtractPatchXMLData auf.
ms.assetid: 85940940-2002-4cb1-8e29-ba2374bf3796
title: Installer.ExtractPatchXMLData-Methode
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
ms.openlocfilehash: d9b4df7d2ecedda5e3bac97a1dd80a002571f736ceb2ede6b8deac2f1a5f7802
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118631543"
---
# <a name="installerextractpatchxmldata-method"></a>Installer.ExtractPatchXMLData-Methode

Die **ExtractPatchXMLData-Methode** des [**Installer-Objekts**](installer-object.md) extrahiert Informationen aus einem Patch als XML-Zeichenfolge. Die Informationen können verwendet werden, um zu bestimmen, ob der Patch auf einem Zielsystem angewendet wird. Diese Methode ruft [**MsiExtractPatchXMLData auf.**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)

## <a name="syntax"></a>Syntax


```JScript
Installer.ExtractPatchXMLData(
  PatchPath
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*PatchPath* 
</dt> <dd>

Vollständiger Pfad zum Patch, aus dem die Anwendbarkeitsinformationen extrahiert werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installer 3.0 oder höher auf Windows Server 2003 oder Windows XP.<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                    |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                                         |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**MsiExtractPatchXMLData**](/windows/desktop/api/Msi/nf-msi-msiextractpatchxmldataa)
</dt> <dt>

[Nicht unterstützt in Windows Installer 2.0 und früher](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




