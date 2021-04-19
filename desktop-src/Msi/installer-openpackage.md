---
description: Mit der OpenPackage-Methode des Installer-Objekts wird ein Installer-Paket für die Verwendung mit Funktionen geöffnet, die auf die Produktdatenbank und die Installations-Engine zugreifen und ein Sitzungs Objekt zurückgeben.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Installer. OpenPackage-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106350775"
---
# <a name="installeropenpackage-method"></a>Installer. OpenPackage-Methode

Mit der **OpenPackage** -Methode des [**Installer**](installer-object.md) -Objekts wird ein Installer-Paket für die Verwendung mit Funktionen geöffnet, die auf die Produktdatenbank und die Installations-Engine zugreifen und ein [**Sitzungs**](session-object.md) Objekt zurückgeben.

## <a name="syntax"></a>Syntax


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*packagePath* 
</dt> <dd>

Erforderliche Zeichenfolge, die den Pfadnamen des Pakets enthält.

</dd> <dt>

*options* 
</dt> <dd>

Ein optionaler ganzzahliger Wert, der angibt, ob **OpenPackage** beim Erstellen des Sitzungs Objekts den aktuellen Computer Zustand ignorieren soll. Kein Wert oder der Wert 0 für Optionen ist standardmäßig auf das ursprüngliche Verhalten eingestellt. Wenn die Option 1 ist, ignoriert die **OpenPackage** -Methode den aktuellen Computer Status beim Öffnen des Pakets. Der Wert 1 verhindert Änderungen am aktuellen Computer Zustand. Weitere Informationen finden Sie unter [**msiopenpackageex**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Die **OpenPackage** -Methode kann das Daten Bank handle direkt anstelle der Zeichenfolge für den Paketpfad akzeptieren.

Beachten Sie, dass nur ein [**Sitzungs**](session-object.md) Objekt von einem einzelnen Prozess geöffnet werden kann. **OpenPackage** kann nicht in einer benutzerdefinierten Aktion verwendet werden, da die aktive Installation die einzige zulässige Sitzung ist.

Ein sicheres [**Sitzungs**](session-object.md) Objekt ignoriert den aktuellen Computer Zustand beim Öffnen des Pakets und verhindert Änderungen am aktuellen Computer Status. Weitere Informationen finden Sie unter [**msiopenpackageex**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




