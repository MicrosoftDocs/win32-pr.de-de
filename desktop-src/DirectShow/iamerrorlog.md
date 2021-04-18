---
description: Die iamerrorlog-Schnittstelle stellt eine Rückruf Methode für die Fehler Protokollierung in DirectShow-Bearbeitungs Diensten bereit. Von des wird diese Schnittstelle nicht implementiert.
ms.assetid: d5366072-2de7-437c-b198-cbc4d8623c45
title: Iamerrorlog-Schnittstelle (qedit. h)
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
ms.openlocfilehash: 48a1515ebf3e7c829a3e23772f1f84ee76c36ae0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372328"
---
# <a name="iamerrorlog-interface"></a>Iamerrorlog-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die- `IAMErrorLog` Schnittstelle stellt eine Rückruf Methode für die Fehler Protokollierung in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) bereit.

Von des wird diese Schnittstelle nicht implementiert. Um die Fehler Protokollierung auszuführen, implementieren Sie diese Schnittstelle in der Anwendung, und nennen Sie [**iamseterrorlog::p UT \_ ErrorLog**](iamseterrorlog-put-errorlog.md) auf der Zeitachse. Wenn beim Rendering des Projekts ein Fehler auftritt, ruft der die [**iamerrorlog:: LogError**](iamerrorlog-logerror.md) -Methode auf, die von der Anwendung implementiert wird.

DES protokolliert Fehler nur, wenn Sie ein Projekt mit der " [**unenderengine**](irenderengine.md) "-Schnittstelle Rendering. Wenn Sie z. b. ein Projekt als DirectShow-Filter Diagramm (GRF-Format) speichern und die Diagramm Datei wiedergeben, gibt es keine Fehler Protokollierung. Weitere Informationen zur Verwendung dieser Schnittstelle finden Sie unter [Protokollieren von Fehlern](logging-errors.md).

## <a name="members"></a>Member

Die **iamerrorlog** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamerrorlog** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamerrorlog** -Schnittstelle verfügt über diese Methoden.



| Methode                                   | BESCHREIBUNG               |
|:-----------------------------------------|:--------------------------|
| [**LogError**](iamerrorlog-logerror.md) | Protokolliert einen Fehler.<br/> |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



 

 
