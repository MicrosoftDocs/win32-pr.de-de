---
UID: NN:dwrite_3.IDWriteBitmapRenderTarget2
title: IDWriteBitmapRenderTarget2 (dwrite_3.h)
description: Kapselt eine geräteunabhängige 32-Bit-Bitmap und einen Gerätekontext, die zum Rendern von Glyphen verwendet werden können.
tech.root: DirectWrite
ms.date: 11/11/2020
ms.topic: reference
req.header: dwrite_3.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: ''
targetos: Windows
req.typenames: ''
req.redist: ''
f1_keywords:
- IDWriteBitmapRenderTarget2
- dwrite_3/IDWriteBitmapRenderTarget2
dev_langs:
- c++
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dwrite.dll
api_name:
- IDWriteBitmapRenderTarget2
ms.openlocfilehash: e12bceefd7ffb89a427edc04b4910b6346dfb066
ms.sourcegitcommit: d7e9a20168111fb608f5fefb092b30f8e093d816
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107881819"
---
# <a name="idwritebitmaprendertarget2-interface-dwrite_3h"></a>IDWriteBitmapRenderTarget2-Schnittstelle (dwrite_3.h)

Kapselt eine geräteunabhängige 32-Bit-Bitmap und einen Gerätekontext, die zum Rendern von Glyphen verwendet werden können.

> [!IMPORTANT]
> Diese API ist als Teil der DWriteCore-Implementierung von [DirectWrite](../direct-write-portal.md)verfügbar. DWriteCore ist eine Form von DirectWrite, die auf Windows-Versionen bis hinunter zu Windows 8 läuft und Ihnen die Möglichkeit eröffnet, es plattformübergreifend zu nutzen. Weitere Informationen und Codebeispiele finden Sie unter [Übersicht über DWriteCore.](/windows/win32/DirectWrite/dwrite/dwritecore-overview)

## <a name="inheritance"></a>Vererbung

Die **IDWriteBitmapRenderTarget2-Schnittstelle** erbt von [IDWriteBitmapRenderTarget1.](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1)

## <a name="methods"></a>Methoden

Die **IDWriteBitmapRenderTarget2-Schnittstelle** verfügt über diese Methoden.

| Methode | BESCHREIBUNG |
| ---- |:---- |
| [IDWriteBitmapRenderTarget2::GetBitmapData](./nf-dwrite_3-idwritebitmaprendertarget2-getbitmapdata.md) | Ruft die Pixeldaten von einem Bitmaprenderziel ab. |

## <a name="requirements"></a>Anforderungen
| &nbsp; | &nbsp; |
| ---- |:---- |
| **Unterstützte Mindestversion (Client)** | Windows 10, Project Reunion [Win32-Apps] |
| **Header** | dwrite_3.h (include dwrite_core.h) |