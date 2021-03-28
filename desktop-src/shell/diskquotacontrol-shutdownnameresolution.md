---
description: Fährt den Thread für die Auflösung von Benutzernamen herunter.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: Diskquotacontrol. shutdownnameresolution-Methode (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.ShutdownNameResolution
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0db952a502210e509abeb527b2006eab087434e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041682"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a>Diskquotacontrol. shutdownnameresolution-Methode

Fährt den Thread für die Auflösung von Benutzernamen herunter.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Bemerkungen

Der sicherheitsbezeichnerresolver übersetzt sid in Benutzernamen in einem Hintergrund Thread. Dieser Thread wird automatisch heruntergefahren, wenn das zugeordnete Kontingent Steuerungsobjekt zerstört wird. Es gibt jedoch einige Fälle, in denen der Thread nicht mehr benötigt wird, aber das Objekt noch nicht zerstört werden kann. Ein typisches Beispiel ist, wenn keine weitere Verarbeitung stattfindet, Clients jedoch weiterhin Verweise auf das Objekt enthalten. Die **shutdownnameresolution** -Methode ermöglicht es Ihnen, den Konflikt Löser-Thread zu beenden und die zugeordneten Ressourcen freizugeben, ohne das Kontingent Steuerungsobjekt zu zerstören.

> [!Note]  
> Wenn Sie den Konflikt Löser-Thread beenden, wird die asynchrone Namensauflösung sofort beendet. Wenn später Aufrufe an Methoden wie " [**adduser**](diskquotacontrol-adduser.md) " oder " [**FINDUSER**](diskquotacontrol-finduser.md)" durchgeführt werden, kann das Kontingent Objekt den resolverthread neu erstellen.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5,0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Diskquotacontrol-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




