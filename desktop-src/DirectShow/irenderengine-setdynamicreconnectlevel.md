---
description: Die setdynamikreconnectlevel-Methode legt die Ebene der dynamischen erneuten Verbindung während des Renderings fest.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: 'Unenderengine:: setdynamikreconnectlevel-Methode (qedit. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine.SetDynamicReconnectLevel
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: ae02fb6158b58cd5785aa7df539651acfbea5db8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368662"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a>Unenderengine:: setdynamikreconnectlevel-Methode

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `SetDynamicReconnectLevel` Methode legt die Ebene der dynamischen erneuten Verbindung während des Renderings fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDynamicReconnectLevel(
   DWORD Level
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Level* 
</dt> <dd>

Kombination [**dynamischer reverbindungsflags**](dynamic-reconnection-flags.md), die die Ebene der dynamischen erneuten Verbindung angeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT** -Werte zurück:



| Rückgabecode                                                                               | Beschreibung                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>         |
| <dl> <dt>**E \_ notimpl**</dt> </dl> | Nicht implementiert.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Standardmäßig lädt die einfache Renderingengine jede Quelle, bevor ein Projekt gerendert wird. Dies kann zu einer langen Start Zeit führen. Bei der dynamischen erneuten Verbindungs Herstellung werden Quellen nur bei Bedarf geladen. Dies kann die Startzeit verkürzen, aber möglicherweise die reibungslose Wiedergabe beeinträchtigen. Im Allgemeinen können Sie von der dynamischen erneuten Verbindung profitieren, umso mehr Quell Clips werden von einem Projekt verwendet.

Diese Methode wird von der Smart-Rendering-Engine nicht implementiert.

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstelle ""**](irenderengine.md)
</dt> <dt>

[Fehler-und Erfolgs Codes](error-and-success-codes.md)
</dt> </dl>

 

 




