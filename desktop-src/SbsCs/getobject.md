---
description: Die GetObject-Methode ruft eine Instanz eines vorhandenen Microsoft. Windows. ActCtx-Objekts ab.
ms.assetid: 547525f3-afef-463b-823a-df8ccd954f36
title: ActCtx. GetObject-Methode
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
ms.openlocfilehash: 11b71d8d40d947472612c91f70e9956aa7798806
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103750961"
---
# <a name="actctxgetobject-method"></a>ActCtx. GetObject-Methode

Die **GetObject** -Methode ruft eine Instanz eines vorhandenen [**Microsoft. Windows. ActCtx**](microsoft-windows-actctx-object.md) -Objekts ab.

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

Erforderliche Zeichenfolge, die das Objekt angibt. Der Name muss sich in der Registrierung unter **HKEY \_ local \_ Machine** \\ **Microsoft** \\ **Visual Studio** \\ **6,0** \\ **<package>** \\ **Automation** befinden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Methode gibt keinen Wert zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                       |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Sxsoa.dll</dt> </dl> |
| IID<br/>                      | IID \_ iactctx ist als 8fa7728f-b69b-4ee5-99f 2-e2aa021bef 28 definiert.<br/>           |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Methode "kreateobject"**](createobject.md)
</dt> </dl>

 

 




