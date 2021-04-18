---
description: Die addsource-Methode des Installer-Objekts fügt der Liste der gültigen Netzwerk Quellen in der SourceList eine Quelle hinzu.
ms.assetid: e24c8484-fe84-4f97-9c06-c063bb7c6810
title: Installer. addsource-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AddSource
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3067ae287311c6ed26b509545523db75a3fed4cf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372391"
---
# <a name="installeraddsource-method"></a>Installer. addsource-Methode

Die **addsource** -Methode des [**Installer**](installer-object.md) -Objekts fügt der Liste der gültigen Netzwerk Quellen in der SourceList eine Quelle hinzu.

## <a name="syntax"></a>Syntax


```JScript
Installer.AddSource(
  Product,
  User,
  Source
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

</dd> <dt>

*Quelle* 
</dt> <dd>

Ein Zeiger auf die Zeichenfolge, die die Quelle angibt.

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

[**Msisourcelistaddsource**](/windows/desktop/api/Msi/nf-msi-msisourcelistaddsourcea)
</dt> <dt>

[Quellen Resilienz](source-resiliency.md)
</dt> </dl>

 

 




