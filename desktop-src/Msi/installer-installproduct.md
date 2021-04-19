---
description: Mit der installproduct-Methode des Installer-Objekts wird ein Installer-Paket geöffnet und eine Installationssitzung initialisiert.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Installer. installproduct-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106355890"
---
# <a name="installerinstallproduct-method"></a>Installer. installproduct-Methode

Mit der **installproduct** -Methode des [**Installer**](installer-object.md) -Objekts wird ein Installer-Paket geöffnet und eine Installationssitzung initialisiert.

## <a name="syntax"></a>Syntax


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*packagePath* 
</dt> <dd>

Erforderliche Zeichenfolge, die den Pfad zum Installationspaket enthält.

</dd> <dt>

*propertyValues* 
</dt> <dd>

Optionale Zeichenfolge, die Eigenschaft = Wert-Paare enthält, getrennt durch Leerraum.

Um eine administrative Installation auszuführen, schließen Sie action = admin in *propertyValues* ein. Weitere Informationen finden Sie unter der [**Action**](action.md) -Eigenschaft.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Wenn Sie ein Produkt vollständig entfernen möchten, legen Sie Remove = All in *propertyValues* fest. Weitere Informationen finden Sie unter [**Remove**](remove.md) -Eigenschaft.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




