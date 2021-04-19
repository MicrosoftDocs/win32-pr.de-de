---
description: Die collectuserinfo-Methode des Installer-Objekts Ruft eine Assistenten Sequenz für eine Benutzeroberfläche auf, die sowohl Benutzerinformationen als auch den Produktcode sammelt und speichert.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Installer. collectuserinfo-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.CollectUserInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d7286fdbc9fab6b3db6752284bf86db05f920bd7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106370159"
---
# <a name="installercollectuserinfo-method"></a>Installer. collectuserinfo-Methode

Die **collectuserinfo** -Methode des [**Installer**](installer-object.md) -Objekts Ruft eine Assistenten Sequenz für eine Benutzeroberfläche auf, die sowohl Benutzerinformationen als auch den Produktcode sammelt und speichert.

## <a name="syntax"></a>Syntax


```JScript
Installer.CollectUserInfo(
  Product
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Produkt* 
</dt> <dd>

Gibt den [**Produktcode**](productcode.md) des Produkts an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Eine Anwendung sollte die Methode **collectuserinfo** beim ersten Ausführen aufzurufen. Mit der **collectuserinfo** -Methode wird das Installationspaket des Produkts geöffnet, und es wird eine erstellte Assistenten Sequenz aufgerufen, die Benutzerinformationen sammelt. Nach Abschluss der Assistenten Sequenz werden die gesammelten Benutzerinformationen registriert. Die [**uilevel**](installer-uilevel.md) -Eigenschaft sollte auf msiuilevelfull festgelegt werden, da diese API eine erstellte Benutzeroberfläche erfordert.

Die **collectuserinfo** -Methode ruft das [FIRSTRUN-Dialog](firstrun-dialog.md)Feld auf.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ iinstaller ist definiert als 000c1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Msicollectuserinfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




