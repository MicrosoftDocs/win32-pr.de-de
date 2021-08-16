---
description: Die CollectUserInfo-Methode des Installer-Objekts ruft eine Benutzeroberflächen-Assistentensequenz auf, die sowohl Benutzerinformationen als auch den Produktcode sammelt und speichert.
ms.assetid: 2faacf38-1af1-4e8a-a3f6-87733104614e
title: Installer.CollectUserInfo-Methode
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
ms.openlocfilehash: 255f9c5bfbd9f7ed476314e8ac1c9ed58568c083b8f6ea7704bbe5cfef15b769
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118632917"
---
# <a name="installercollectuserinfo-method"></a>Installer.CollectUserInfo-Methode

Die **CollectUserInfo-Methode** des [**Installer-Objekts**](installer-object.md) ruft eine Benutzeroberflächen-Assistentensequenz auf, die sowohl Benutzerinformationen als auch den Produktcode sammelt und speichert.

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

Gibt den [**Produktcode des**](productcode.md) Produkts an.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Eine Anwendung sollte die **CollectUserInfo-Methode bei** der ersten Ausführung aufrufen. Die **CollectUserInfo-Methode** öffnet das Installationspaket des Produkts und ruft eine Sequenz des Assistenten für die benutzeroberfläche auf, die Benutzerinformationen sammelt. Nach Abschluss der Assistentensequenz werden die gesammelten Benutzerinformationen registriert. Die [**UILevel-Eigenschaft**](installer-uilevel.md) sollte auf msiUILevelFull festgelegt werden, da für diese API eine benutzeroberfläche erforderlich ist.

Die **CollectUserInfo-Methode** ruft den [FirstRun-Dialog auf.](firstrun-dialog.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5.0 auf Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4.0 oder Windows Installer 4.5 auf Windows Server 2008 oder Windows Vista. Windows Installationsprogramm auf Windows Server 2003 oder Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller ist als 000C1090-0000-0000-C000-00000000046 definiert.<br/>                                                                                                                                                                           |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**MsiCollectUserInfo**](/windows/desktop/api/Msi/nf-msi-msicollectuserinfoa)
</dt> </dl>

 

 




