---
description: Fährt den Thread für die Benutzernamenauflösung herunter.
ms.assetid: 6c4544b9-81e7-4a72-aa00-70011e5cd85a
title: DiskQuotaControl.ShutdownNameResolution-Methode (Dskquota.h)
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
ms.openlocfilehash: da02f79ea8f7b582056e9c3c7c0c3f1db53fa9e08181559c99dd983924861c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459837"
---
# <a name="diskquotacontrolshutdownnameresolution-method"></a>DiskQuotaControl.ShutdownNameResolution-Methode

Fährt den Thread für die Benutzernamenauflösung herunter.

## <a name="syntax"></a>Syntax


```JScript
DiskQuotaControl.ShutdownNameResolution()
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="remarks"></a>Hinweise

Der Sid-Namensre resolver (Sicherheits-ID) übersetzt SID in Benutzernamen in einem Hintergrundthread. Dieser Thread wird automatisch heruntergefahren, wenn das zugeordnete Kontingentsteuerungsobjekt zerstört wird. Es gibt jedoch einige Fälle, in denen der Thread nicht mehr benötigt wird, das Objekt aber noch nicht bereit ist, zerstört zu werden. Ein typisches Beispiel ist, wenn keine weitere Verarbeitung stattfindet, clients aber weiterhin Verweise auf das -Objekt enthalten. Mit **der ShutdownNameResolution-Methode** können Sie den Konfliktlöserthread beenden und die zugeordneten Ressourcen frei geben, ohne das Kontingentsteuerungsobjekt zu zerstören.

> [!Note]  
> Wenn Sie den Resolverthread herunterfahren, wird die asynchrone Namensauflösung sofort beendet. Wenn anschließend Aufrufe an Methoden wie [**AddUser**](diskquotacontrol-adduser.md) oder [**FindUser**](diskquotacontrol-finduser.md)vorgenommen werden, erstellt das Kontingentobjekt möglicherweise den Konfliktlöserthread neu.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                                          |
| Header<br/>                   | <dl> <dt>Dskquota.h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (Version 5.0 oder höher)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DiskQuotaControl-Objekt**](diskquotacontrol-object.md)
</dt> </dl>

 

 




