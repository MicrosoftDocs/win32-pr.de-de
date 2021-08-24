---
description: Die IAMErrorLog-Schnittstelle stellt eine Rückrufmethode für die Fehlerprotokollierung in DirectShow Editing Services (DES) bereit. Des implementiert diese Schnittstelle nicht.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: IAMErrorLog-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMErrorLog
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: f2edd1d315cc7ae35bbc200209667d49d53392ce86a10b40a067182cd0621124
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119756460"
---
# <a name="iamerrorlog-interface"></a>IAMErrorLog-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Die `IAMErrorLog` -Schnittstelle stellt eine Rückrufmethode für die Fehlerprotokollierung in [DirectShow Editing Services](directshow-editing-services.md) (DES) bereit.

Des implementiert diese Schnittstelle nicht. Implementieren Sie zum Ausführen der Fehlerprotokollierung diese Schnittstelle in Ihrer Anwendung, und rufen Sie [**IAMSetErrorLog::p ut \_ ErrorLog**](iamseterrorlog-put-errorlog.md) auf der Zeitachse auf. Wenn beim Rendern des Projekts ein Fehler auftritt, ruft DES die [**IAMErrorLog::LogError-Methode**](iamerrorlog-logerror.md) auf, die von Ihrer Anwendung implementiert wird.

DES protokolliert Fehler nur, wenn Sie ein Projekt mithilfe der [**IRenderEngine-Schnittstelle rendern.**](irenderengine.md) Wenn Sie beispielsweise ein Projekt als DirectShow-Filtergraph (GRF-Format) speichern und die Graphdatei wiedergeben, erfolgt keine Fehlerprotokollierung. Weitere Informationen zur Verwendung dieser Schnittstelle finden Sie unter [Protokollierungsfehler.](logging-errors.md)

## <a name="members"></a>Member

Die **IAMErrorLog-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IAMErrorLog** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IAMErrorLog-Schnittstelle** verfügt über diese Methoden.



| Methode                                   | Beschreibung               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | Protokolliert einen Fehler.<br/> |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern kompatibel, die höher als Version 7 sind.

 

> [!Note]  
> Laden Sie zum Abrufen von Qedit.h das [Microsoft Windows SDK-Update für Windows Vista und .NET Framework 3.0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
