---
description: Das GetFiles-Objekt ruft die erforderlichen Dateien in einer bestimmten Sprache des Moduls ab. Erfordert, dass bestimmte Aktionen über das Merge-Objekt durchgeführt werden, bevor alle Teile dieser Schnittstelle gültige Ergebnisse zurückgeben.
ms.assetid: f3bf64ec-75f7-43a6-bbd8-a51508c57002
title: GetFiles-Objekt (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFiles
- IMsmGetFiles
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 8a26bb072b0b4a1f048ded76fbd52ffc6d42de62
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369260"
---
# <a name="getfiles-object"></a>GetFiles-Objekt

Das **GetFiles** -Objekt ruft die erforderlichen Dateien in einer bestimmten Sprache des Moduls ab. Erfordert, dass bestimmte Aktionen über das [Merge-Objekt](merge-object.md) durchgeführt werden, bevor alle Teile dieser Schnittstelle gültige Ergebnisse zurückgeben.

## <a name="members"></a>Member

Das **GetFiles** -Objekt verfügt über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Das **GetFiles** -Objekt verfügt über diese Eigenschaften.



| Eigenschaft                                               | BESCHREIBUNG                                                                                                                                                     |
|:-------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Modulefiles**](getfiles-modulefiles.md)<br/> | Die [**Modulefiles**](getfiles-modulefiles.md) -Eigenschaft gibt alle Primärschlüssel der [Dateitabelle](file-table.md) für das aktuell geöffnete Modul zurück.<br/> |



 

## <a name="c"></a>C++

Schnittstelle **imsmgetfiles: IDispatch**

## <a name="interface-id"></a>Schnittstellen-ID



| Konstante              | Wert                                  |
|-----------------------|----------------------------------------|
| **IID \_ imsmgetfiles** | {7041ae26-2d78-11d2-888a-00a0c981b015} |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Version<br/> | Mergemod.dll 1,0 oder höher<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




