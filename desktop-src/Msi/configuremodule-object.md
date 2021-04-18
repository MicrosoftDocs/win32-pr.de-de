---
description: Das "Konfigurationsmodul"-Objekt ist eine vom Client implementierte Schnittstelle.
ms.assetid: f6240837-7685-4bfe-8a2f-b4428014702a
title: Konfigurationsmodul-Objekt (Mergemod. h)
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
ms.openlocfilehash: 0c99f8932d1d3c0e7ba7d7df5e14fc0738e8b81c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106352117"
---
# <a name="configuremodule-object"></a>"Konfiguriermodule"-Objekt

Das " **Konfigurationsmodul** "-Objekt ist eine vom Client implementierte Schnittstelle. Mergemod.dllruft Methoden auf der **imsmkonfigurremodule** -Schnittstelle auf, um anzufordern, dass das Client Tool Konfigurationsinformationen bereitstellt. Das Modul wird auf der Grundlage der Client Antworten auf Aufrufe dieser Schnittstelle konfiguriert.

## <a name="members"></a>Member

Das Objekt " **Konfigurationsmodul** " verfügt über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Das Objekt " **konfigurierungsmodul** " verfügt über diese Methoden.



| Methode                                                           | BESCHREIBUNG                                                                        |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------|
| [**Provideintegerdata**](configuremodule-provideintegerdata.md) | Wird von Mergemod.dll aufgerufen, um ganze Zahlen zu erhalten, die zum Konfigurieren des Moduls verwendet werden.<br/> |
| [**Provide TextData**](configuremodule-providetextdata.md)       | Wird von Mergemod.dll aufgerufen, um Text zu erhalten, der zum Konfigurieren des Moduls verwendet wird.<br/>     |



 

## <a name="remarks"></a>Bemerkungen

### <a name="c"></a>C++

Schnittstelle **imsmkonfiguriermodule: IDispatch**

### <a name="interface-id"></a>Schnittstellen-ID



| Konstante                     | Wert                                  |
|------------------------------|----------------------------------------|
| **IID \_ imsmkonfiguriterremodule** | {AC013209-18A7-4851-8A21-2353443D70A0} |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 2,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




