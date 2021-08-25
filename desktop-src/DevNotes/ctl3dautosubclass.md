---
description: Automatisches Unterklassen und Hinzufügen von 3D-Effekten zu allen Dialogfeldern in der Anwendung.
ms.assetid: 96555052-c564-4cc7-9b24-e527f8e2f879
title: Ctl3dAutoSubclass-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Ctl3dAutoSubclass
api_type:
- DllExport
api_location:
- Ctl3d32.dll
ms.openlocfilehash: 5edc8bafb00d5444f18b61e0600fb075b6a7367c315c2ab1cfe38f911e9a84d9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654610"
---
# <a name="ctl3dautosubclass-function"></a>Ctl3dAutoSubclass-Funktion

Automatisches Unterklassen und Hinzufügen von 3D-Effekten zu allen Dialogfeldern in der Anwendung.

## <a name="syntax"></a>Syntax


```C++
PUBLIC BOOL FAR PASCAL Ctl3dAutoSubclass(
   HANDLE hinstApp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*hinstApp* 
</dt> <dd>

Ein Handle für die Anwendung, die als Client registriert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt **TRUE** zurück, es sei denn, eine der folgenden Bedingungen ist vorhanden. In diesem Fall wird **FALSE** zurückgegeben:

-   CTL3D wird unter Windows Version 3.0 oder früher ausgeführt.
-   Für CTL3D ist in den Tabellen für die aktuelle Anwendung kein Speicherplatz verfügbar. CTL3D kann bis zu 32 Anwendungen gleichzeitig bedienen.
-   CTL3D kann den CBT-Hook nicht installieren.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|----------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Ctl3d32.dll</dt> </dl> |



 

 
