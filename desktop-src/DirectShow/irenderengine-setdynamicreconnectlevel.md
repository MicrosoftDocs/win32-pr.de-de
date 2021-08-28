---
description: Die SetDynamicReconnectLevel-Methode legt die Ebene der dynamischen wiederhergestellten Verbindung während des Renderings fest.
ms.assetid: 092f3464-84a2-48b0-9647-66fe27e9706d
title: IRenderEngine::SetDynamicReconnectLevel-Methode (Qedit.h)
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
ms.openlocfilehash: b43967753dd03d213a322ce569d113346542a57b5f37fd69fc28937198109049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083680"
---
# <a name="irenderenginesetdynamicreconnectlevel-method"></a>IRenderEngine::SetDynamicReconnectLevel-Methode

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die `SetDynamicReconnectLevel` -Methode legt die Ebene der dynamischen wiederhergestellten Verbindung während des Renderings fest.

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

Kombination von [**Dynamic Reconnection-Flags,**](dynamic-reconnection-flags.md)die die Ebene der dynamischen wiederhergestellten Verbindung angeben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Gibt einen der folgenden **HRESULT-Werte** zurück:



| Rückgabecode                                                                               | Beschreibung                 |
|-------------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Erfolg.<br/>         |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | Nicht implementiert.<br/> |



 

## <a name="remarks"></a>Hinweise

Standardmäßig lädt die einfache Render-Engine jede Quelle, bevor ein Projekt gerendert wird. Dies kann zu einer langen Startzeit führen. Bei der dynamischen wiederhergestellten Verbindung werden Quellen nur bei Bedarf geladen. Dies kann die Startzeit kürzen, aber möglicherweise die reibungslose Wiedergabe beeinträchtigen. Im Allgemeinen gilt: Wenn ein Projekt mehr Quellclips verwendet, können Sie von der dynamischen Wiederherstellung der Verbindung profitieren.

Die intelligente Render-Engine implementiert diese Methode nicht.

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IRenderEngine-Schnittstelle**](irenderengine.md)
</dt> <dt>

[Fehler- und Erfolgscodes](error-and-success-codes.md)
</dt> </dl>

 

 




