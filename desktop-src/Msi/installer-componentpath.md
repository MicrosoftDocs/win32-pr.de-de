---
description: Die ComponentPath-Eigenschaft ist eine schreibgeschützte Eigenschaft, die den vollständigen Pfad zu einer installierten Komponente zurückgibt. Wenn der Schlüsselpfad für die Komponente ein Registrierungsschlüssel ist, wird der Registrierungsschlüssel zurückgegeben.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Installer.ComponentPath-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ComponentPath
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 88601dc4c65d0d3f69a5386ed62d1523c9fa21723e73b1ad4d208d0eff437658
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632623"
---
# <a name="installercomponentpath-property"></a>Installer.ComponentPath-Eigenschaft

Die **ComponentPath-Eigenschaft** ist eine schreibgeschützte Eigenschaft, die den vollständigen Pfad zu einer installierten Komponente zurückgibt. Wenn der Schlüsselpfad für die Komponente ein Registrierungsschlüssel ist, wird der Registrierungsschlüssel zurückgegeben.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Hinweise

Wenn die Komponente ein Registrierungsschlüssel ist, werden die Stammverzeichnis der Registrierung numerisch dargestellt. Beispielsweise wird der Registrierungspfad "HKEY \_ CURRENT \_ USER SOFTWARE \\ \\ Microsoft" als "01: \\ SOFTWARE \\ Microsoft" zurückgegeben. Die zurückgegebenen Registrierungsstammdateien werden wie folgt definiert:



| Root                    | Rückgabewert |
|-------------------------|----------------|
| HKEY \_ CLASSES \_ ROOT     | 00             |
| AKTUELLER \_ \_ HKEY-BENUTZER     | 01             |
| HKEY \_ LOCAL \_ MACHINE    | 02             |
| \_HKEY-BENUTZER             | 03             |
| \_HKEY-LEISTUNGSDATEN \_ | 04             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installationsprogramm 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-0000000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




