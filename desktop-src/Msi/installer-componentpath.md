---
description: Die componentpath-Eigenschaft ist eine schreibgeschützte Eigenschaft, die den vollständigen Pfad zu einer installierten Komponente zurückgibt. Wenn der Schlüssel Pfad für die Komponente ein Registrierungsschlüssel ist, wird der Registrierungsschlüssel zurückgegeben.
ms.assetid: 6e53419d-f28a-45cd-abc8-0f451177f3fc
title: Installer. componentpath (Eigenschaft)
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
ms.openlocfilehash: e249290af2477d2dfcbc73f80f80b439f1dd3663
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106361961"
---
# <a name="installercomponentpath-property"></a>Installer. componentpath (Eigenschaft)

Die **componentpath** -Eigenschaft ist eine schreibgeschützte Eigenschaft, die den vollständigen Pfad zu einer installierten Komponente zurückgibt. Wenn der Schlüssel Pfad für die Komponente ein Registrierungsschlüssel ist, wird der Registrierungsschlüssel zurückgegeben.

Diese Eigenschaft ist schreibgeschützt.

## <a name="syntax"></a>Syntax


```JScript
propVal = Installer.ComponentPath
```



## <a name="property-value"></a>Eigenschaftswert

## <a name="remarks"></a>Bemerkungen

Wenn es sich bei der Komponente um einen Registrierungsschlüssel handelt, werden die Registrierungs Stämme numerisch dargestellt. Beispielsweise würde der Registrierungs Pfad "HKEY \_ Current \_ User \\ Software \\ Microsoft" als "01: \\ Software Microsoft" zurückgegeben werden \\ . Die zurückgegebenen Registrierungs Stämme werden wie folgt definiert:



| Root                    | Rückgabewert |
|-------------------------|----------------|
| HKEY- \_ Klassen Stamm \_     | 00             |
| Aktueller HKEY- \_ \_ Benutzer     | 01             |
| lokaler HKEY- \_ \_ Computer    | 02             |
| HKEY- \_ Benutzer             | 03             |
| HKEY- \_ Leistungs \_ Daten | 04             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha)
</dt> </dl>

 

 




