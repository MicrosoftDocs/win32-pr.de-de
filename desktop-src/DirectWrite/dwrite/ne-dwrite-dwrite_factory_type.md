---
UID: NE:dwrite.DWRITE_FACTORY_TYPE
title: DWRITE_FACTORY_TYPE (dwrite.h)
description: Gibt den Typ des DirectWrite-factoryobjekts an.
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
ms.openlocfilehash: 603b2ae525ddc6472a3b8581627f2877e06d1aac
ms.sourcegitcommit: dd4a3716477b1363be58ecc0d439029f81467104
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/11/2020
ms.locfileid: "104040028"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>DWRITE_FACTORY_TYPE-Enumeration (dwrite. h)

Gibt den Typ des DirectWrite-factoryobjekts an.

> [!IMPORTANT]
> Diese API ist als Teil der dwrite-Core-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar. DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen. Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über dbeschreib tecore](/windows/win32/DirectWrite/dwrite/dwritecore-overview).

## <a name="syntax"></a>Syntax
```cpp
typedef enum DWRITE_FACTORY_TYPE {
  DWRITE_FACTORY_TYPE_SHARED,
  DWRITE_FACTORY_TYPE_ISOLATED,
  DWRITE_FACTORY_TYPE_RESTRICTED
} ;
```

## <a name="constants"></a>Konstanten

| Name | BESCHREIBUNG |
| ---- |:---- |
| DWRITE_FACTORY_TYPE_SHARED | Gibt an, dass die DirectWrite-Factory eine freigegebene Factory ist und die Wiederverwendung von zwischengespeicherten Schriftart Daten über mehrere Prozess interne Komponenten hinweg ermöglicht. Diese Factorys nutzen auch prozessübergreifende Schriftart Caching-Komponenten, um die Leistung zu verbessern. |
| DWRITE_FACTORY_TYPE_ISOLATED | Gibt an, dass das DirectWrite-Factoryobjekt isoliert ist. Objekte, die aus der isolierten Factory erstellt werden, interagieren nicht mit dem internen DirectWrite-Status anderer Komponenten. |
| DWRITE_FACTORY_TYPE_RESTRICTED | Objekte, die aus einer eingeschränkten Factory erstellt werden, verwenden weder den internen Zustand noch die von anderen Factorys verwendeten zwischengespeicherten Daten. Außerdem enthält die System Schriftart Auflistung nur bekannte Schriftarten.|

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie im Thema [Übersicht über dbeschreib tecore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) und in der Beispiel-App für [dwrite-coregallery](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery) .

## <a name="remarks"></a>Bemerkungen

Ein DirectWrite-Factoryobjekt enthält Informationen über den internen Zustand, z. b. die Schriftart Lade Modul Registrierung und zwischengespeicherte Schriftart Daten. In den meisten Fällen sollten Sie das freigegebene Factoryobjekt verwenden, da es mehreren Komponenten ermöglicht, die DirectWrite verwenden, um interne DirectWrite-Zustandsinformationen freizugeben, wodurch die Speicherauslastung reduziert wird. Es gibt jedoch Fälle, in denen es wünschenswert ist, die Auswirkungen einer Komponente auf den restlichen Prozess zu reduzieren, z. b. ein Plug-in aus einer nicht vertrauenswürdigen Quelle, durch Sandkasten und deren Isolierung von den restlichen Prozesskomponenten. In solchen Fällen sollten Sie eine isolierte Factory für die Sandbox Komponente verwenden.

Eine eingeschränkte Factory ist besser gesperrt als eine isolierte Factory. Es findet in keiner Weise eine Interaktion mit einem prozessübergreifenden oder permanenten Schriftart Cache. Außerdem enthält die von dieser Factory zurückgegebene System Schriftart Auflistung nur bekannte Schriftarten. Wenn Sie **DWRITE_FACTORY_TYPE_RESTRICTED** an eine Version von dwrite übergeben, die älter als dwrite-Core ist, gibt [dschreitekreatefactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) **E_INVALIDARG** zurück.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Project Reunion 0,1-Vorabversion [Win32-Apps] |
| **Header** | dwrite. h (Include dwrite_core. h) |
