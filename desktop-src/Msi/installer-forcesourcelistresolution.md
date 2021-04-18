---
description: Die forcesourcelistresolution-Methode des Installer-Objekts erzwingt das Windows Installer, die Quell Liste nach einer gültigen Produkt Quelle zu durchsuchen.
ms.assetid: d5097331-8cf5-494f-9e88-bcffcad3fe5d
title: Installer. forcesourcelistresolution-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ForceSourceListResolution
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: cadc27f3eaa90cd6fb2729f73d07cbcfa1f96b73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106364789"
---
# <a name="installerforcesourcelistresolution-method"></a>Installer. forcesourcelistresolution-Methode

Die **forcesourcelistresolution** -Methode des [**Installer**](installer-object.md) -Objekts erzwingt, dass das Installationsprogramm die Quell Liste nach einer gültigen Produkt Quelle durchsucht, wenn eine Quelle das nächste Mal benötigt wird, z. b. wenn das Installationsprogramm eine Installation oder eine Neuinstallation ausführt oder wenn der Pfad für die Ausführung einer Komponente von der Quelle benötigt wird.

## <a name="syntax"></a>Syntax


```JScript
Installer.ForceSourceListResolution(
  Product,
  User
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Produkt* 
</dt> <dd>

Gibt den Produktcode an.

</dd> <dt>

*Benutzer* 
</dt> <dd>

Benutzername für die Installation pro Benutzer NULL oder eine leere Zeichenfolge für die Installation pro Computer.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msisourcelistforceresolution**](/windows/desktop/api/Msi/nf-msi-msisourcelistforceresolutiona)
</dt> <dt>

[Quellen Resilienz](source-resiliency.md)
</dt> </dl>

 

 




