---
description: Das ConfigureModule-Objekt ist eine schnittstelle, die vom Client implementiert wird.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: ConfigureModule-Objekt (Mergemod.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 7685ce1f1c9c7d8f519395c578000375742eea49dd169085e99c582e14c35a29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143711"
---
# <a name="configuremodule-object"></a>ConfigureModule-Objekt

Das **ConfigureModule-Objekt** ist eine schnittstelle, die vom Client implementiert wird. Mergemod.dllruft Methoden auf der **IMsmConfigureModule-Schnittstelle** auf, um anzufordern, dass das Clienttool Konfigurationsinformationen bereitstellt. Das Modul wird basierend auf den Antworten des Clients auf Aufrufe dieser Schnittstelle konfiguriert.

## <a name="members"></a>Member

Das **ConfigureModule-Objekt** verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das **ConfigureModule-Objekt** verfügt über diese Methoden.



| Methode                                                           | Beschreibung                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**ProvideIntegerData**](configuremodule-provideintegerdata.md) | Wird von Mergemod.dll aufgerufen, um ganze Zahlen abzurufen, die zum Konfigurieren des Moduls verwendet werden.<br/> |
| [**ProvideTextData**](configuremodule-providetextdata.md)       | Wird von Mergemod.dll aufgerufen, um Text abzurufen, der zum Konfigurieren des Moduls verwendet wird.<br/>     |



 

## <a name="remarks"></a>Hinweise

### <a name="c"></a>C++

schnittstelle **IMsmConfigureModule : IDispatch**

### <a name="interface-id"></a>Schnittstellen-ID



| Konstante                     | Wert                                  |
|------------------------------|----------------------------------------|
| **\_IID-IMsmConfigureModule** | {AC013209-18A7-4851-8A21-2353443D70A0} |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2.0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




