---
UID: NE:dwrite_core.DWriteCoreCreateFactory
title: DWriteCoreCreateFactory (dwrite_core.h)
description: Erstellt ein Factoryobjekt, das für die nachfolgende Erstellung einzelner DWriteCore-Objekte verwendet wird.
tech.root: DirectWrite
ms.date: 04/21/2021
ms.topic: reference
req.header: dwrite_core.h
req.include-header: ''
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
- DWriteCoreCreateFactory
- dwrite_core/DWriteCoreCreateFactory
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- HeaderDef
api_location:
- dwrite_core.h
api_name:
- DWriteCoreCreateFactory
ms.openlocfilehash: 6606ad884fd65195e9922d348cc4fe565b95f2ee
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107882137"
---
# <a name="dwritecorecreatefactory-function-dwrite_coreh"></a>DWriteCoreCreateFactory-Funktion (dwrite_core.h)

Erstellt ein Factoryobjekt, das für die nachfolgende Erstellung einzelner DWriteCore-Objekte verwendet wird.

> [!IMPORTANT]
> Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar. DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen. Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)

## <a name="syntax"></a>Syntax
```cpp
HRESULT DWRITE_EXPORT DWriteCoreCreateFactory(
    _In_ DWRITE_FACTORY_TYPE factoryType,
    _In_ REFIID iid,
    _COM_Outptr_ IUnknown** factory
);
```

## <a name="parameters"></a>Parameter

`factoryType`

Typ: <b> <a href="/windows/win32/api/dwrite/ne-dwrite-dwrite_factory_type">DWRITE_FACTORY_TYPE</a></b>

Ein -Wert, der angibt, ob das Factoryobjekt freigegeben, isoliert oder eingeschränkt wird.

`iid`

Typ: <b>REFIID</b>

Ein GUID-Wert, der die DirectWrite-Factoryschnittstelle identifiziert, z. B. __uuidof(<a href="/windows/win32/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>).

`factory`

Typ: <b>IUnknown**</b>

Eine Adresse eines Zeigers auf das neu erstellte DirectWrite-Factoryobjekt.

## <a name="return-value"></a>Rückgabewert

Typ: <b>HRESULT</b>

Wenn diese Methode erfolgreich ist, wird <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>zurückgegeben. Andernfalls wird ein <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT-Fehlercode</b> zurückgegeben.

## <a name="examples"></a>Beispiele

Weitere Informationen finden Sie im Übersichtsthema [DWriteCore](/windows/win32/DirectWrite/dwrite/dwritecore-overview) und in der [Beispiel-App DWriteCoreGallery.](https://github.com/microsoft/Project-Reunion-Samples/tree/main/DWriteCore/DWriteCoreGallery)

## <a name="remarks"></a>Bemerkungen

Dies entspricht funktional der [DWriteCreateFactory-Funktion,](/windows/win32/api/dwrite/nf-dwrite-dwritecreatefactory) die von der Systemversion von DirectWrite exportiert wird. Die DWriteCore-Funktion hat einen anderen Namen, um Mehrdeutigkeiten zu vermeiden.

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Project Reunion [Win32-Apps] |
| **Header** | dwrite.h (include dwrite_core.h) |
