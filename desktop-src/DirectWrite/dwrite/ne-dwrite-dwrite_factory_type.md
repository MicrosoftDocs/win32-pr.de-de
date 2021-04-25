---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Gibt den Typ des DirectWrite-Factoryobjekts an.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite.h
req.include-header: dwrite_core.h
req.target-type: Windows
req.target-min-winverclnt: ''
req.target-min-winversvr: ''
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: ''
req.dll: ''
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- DWRITE_FACTORY_TYPE
- dwrite/DWRITE_FACTORY_TYPE
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite.h
api_name:
- DWRITE_FACTORY_TYPE
ms.openlocfilehash: 85f74d72dc8799a7a3c78603ec0dd5f9c118fdb1
ms.sourcegitcommit: 7024106e3420607420bb04c3f88d9bb4827038c8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/25/2021
ms.locfileid: "107955003"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>DWRITE_FACTORY_TYPE -Enumeration (dwrite.h)

Gibt den Typ des DirectWrite-Factoryobjekts an.

> [!IMPORTANT]
> Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite verfügbar.](../direct-write-portal.md) DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen. Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](/windows/win32/directwrite/dwritecore-overview)

## <a name="syntax"></a>Syntax
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_ISOLATED2
} ;
```

## <a name="constants"></a>Konstanten

| Name | BESCHREIBUNG |
| ---- |:---- |
| DWRITE_FACTORY_TYPE_SHARED | Gibt an, dass die DirectWrite-Factory eine freigegebene Factory ist und die Wiederverwendung zwischengespeicherter Schriftartdaten über mehrere Prozesskomponenten hinweg ermöglicht. Solche Factorys nutzen auch prozessübergreifende Schriftartzwischenspeicherungskomponenten, um eine bessere Leistung zu erzielen. |
| DWRITE_FACTORY_TYPE_ISOLATED | Gibt an, dass das DirectWrite-Factoryobjekt isoliert ist. Objekte, die aus der isolierten Factory erstellt werden, interagieren nicht mit dem internen DirectWrite-Zustand anderer Komponenten. |
| DWRITE_FACTORY_TYPE_ISOLATED2 | Gibt an, dass das DirectWrite-Factoryobjekt eingeschränkt ist. Objekte, die aus einer eingeschränkten Factory erstellt wurden, verwenden oder ändern weder den internen Zustand noch zwischengespeicherte Daten, die von anderen Factorys verwendet werden. Darüber hinaus enthält die Auflistung der Systemschriftarten nur bekannte Schriftarten.|

## <a name="examples"></a>Beispiele

Weitere Informationen finden [Sie im DWriteCore-Übersichtsthema](/windows/win32/directwrite/dwritecore-overview) und in der [DWriteCoreGallery-Beispiel-App.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="remarks"></a>Hinweise

Ein DirectWrite-Factoryobjekt enthält Informationen über seinen internen Zustand, z. B. die Registrierung des Schriftartladeprogramm und zwischengespeicherte Schriftartdaten. In den meisten Fällen sollten Sie das Shared Factory-Objekt verwenden, da es mehreren Komponenten, die DirectWrite verwenden, die Freigabe interner DirectWrite-Statusinformationen ermöglicht, wodurch die Speicherauslastung reduziert wird. Es gibt jedoch Fälle, in denen es wünschenswert ist, die Auswirkungen einer Komponente auf den Rest des Prozesses zu reduzieren, z. B. ein Plug-In aus einer nicht vertrauenswürdigen Quelle, indem eine Sandbox verwendet und von den restlichen Prozesskomponenten entfernt wird. In solchen Fällen sollten Sie eine isolierte Factory für die Sandboxkomponente verwenden.

Eine eingeschränkte Factory ist stärker gesperrt als eine isolierte Factory. Es interagiert in keiner Weise mit einem prozessübergreifenden oder persistenten Schriftartcache. Darüber hinaus enthält die von dieser Factory zurückgegebene Systemschriftartsammlung nur bekannte Schriftarten. Wenn Sie **DWRITE_FACTORY_TYPE_ISOLATED2** an eine Version von DWrite übergeben, die älter als DWriteCore ist, gibt [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) **E_INVALIDARG** zurück.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Project Reunion [Win32-Apps] |
| **Header** | dwrite.h (include dwrite_core.h) |
