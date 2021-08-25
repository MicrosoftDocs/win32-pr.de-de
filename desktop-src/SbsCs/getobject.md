---
description: Die GetObject-Methode ruft eine Instanz eines vorhandenen Microsoft ab. Windows. ActCtx-Objekt.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx.GetObject-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ActCtx.GetObject
api_type:
- COM
api_location:
- Sxsoa.dll
ms.openlocfilehash: a102fdae74232fa9a67c4b9455050bcdba32a219d8a66180ae8bc6ce6cb96c8c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119885280"
---
# <a name="actctxgetobject-method"></a>ActCtx.GetObject-Methode

Die **GetObject-Methode** ruft eine Instanz eines vorhandenen [**Microsoft.Windows ab. ActCtx-Objekt.**](microsoft-windows-actctx-object.md)

## <a name="syntax"></a>Syntax


```JScript
ActCtx.GetObject(
  bstrName
)
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*bstrName* 
</dt> <dd>

Erforderliche Zeichenfolge, die das Objekt angibt. Der Name muss in der Registrierung unter **HKEY \_ LOCAL \_ MACHINE** \\ **Microsoft** \\ **Visual Studio** \\ **6.0** Automation vorhanden \\ **<package>** \\ sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ IActCtx ist als 8FA7728F-B69B-4EE5-99F2-E2AA021BEF28 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CreateObject-Methode**](createobject.md)
</dt> </dl>

 

 




