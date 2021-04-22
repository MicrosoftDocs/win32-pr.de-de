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
ms.openlocfilehash: 87b0d1c2edcb836afd06d732f242b62441b9bd01
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881809"
---
# <a name="dwrite_factory_type-enumeration-dwriteh"></a>DWRITE_FACTORY_TYPE-Enumeration (dwrite.h)

Gibt den Typ des DirectWrite-Factoryobjekts an.

> [!IMPORTANT]
> Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar. DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen. Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)

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
| DWRITE_FACTORY_TYPE_SHARED | Gibt an, dass die DirectWrite-Factory eine freigegebene Factory ist und die Wiederverwendung zwischengespeicherter Schriftartdaten über mehrere Prozesskomponenten hinweg ermöglicht. Solche Factorys nutzen auch prozessübergreifende Komponenten zum Zwischenspeichern von Schriftarten, um eine bessere Leistung zu erzielen. |
| DWRITE_FACTORY_TYPE_ISOLATED | Gibt an, dass das DirectWrite-Factoryobjekt isoliert ist. Objekte, die aus der isolierten Factory erstellt wurden, interagieren nicht mit dem internen DirectWrite-Zustand anderer Komponenten. |
| DWRITE_FACTORY_TYPE_ISOLATED2 | Gibt an, dass das DirectWrite-Factoryobjekt eingeschränkt ist. Objekte, die aus einer eingeschränkten Factory erstellt werden, verwenden oder ändern weder den internen Zustand noch zwischengespeicherte Daten, die von anderen Factorys verwendet werden. Darüber hinaus enthält die Systemschriftartauflistung nur bekannte Schriftarten.|

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie im Übersichtsthema [DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) und in der [Beispiel-App DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="remarks"></a>Bemerkungen

Ein DirectWrite-Factoryobjekt enthält Informationen über seinen internen Zustand, z. B. die Registrierung des Schriftartladeprogramm und zwischengespeicherte Schriftartdaten. In den meisten Fällen sollten Sie das freigegebene Factoryobjekt verwenden, da es mehreren Komponenten, die DirectWrite verwenden, ermöglicht, interne DirectWrite-Zustandsinformationen freizugeben, wodurch die Speicherauslastung reduziert wird. Es gibt jedoch Fälle, in denen es wünschenswert ist, die Auswirkungen einer Komponente auf den Rest des Prozesses zu reduzieren, z. B. ein Plug-In aus einer nicht vertrauenswürdigen Quelle, indem sie in der Sandbox gespeichert und von den restlichen Prozesskomponenten isolieren wird. In solchen Fällen sollten Sie eine isolierte Factory für die Sandboxkomponente verwenden.

Eine eingeschränkte Factory ist stärker gesperrt als eine isolierte Factory. Es interagiert in irgendeiner Weise nicht mit einem prozessübergreifenden oder beständigen Schriftartcache. Darüber hinaus enthält die von dieser Factory zurückgegebene Auflistung von Systemschriftarten nur bekannte Schriftarten. Wenn Sie **DWRITE_FACTORY_TYPE_ISOLATED2** DWrite-Version übergeben, die älter als DWriteCore ist, gibt [DWriteCreateFactory](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) **E_INVALIDARG.**

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Project Reunion [Win32-Apps] |
| **Header** | dwrite.h (include dwrite_core.h) |
