---
description: Die iamtimelinecomp-Schnittstelle fügt virtuelle Spuren in einer Komposition in DirectShow-Bearbeitungs Diensten ein bzw. ruft Sie ab. Eine Komposition ist eine Auflistung von Ebenen, die als einzelner, zusammengesetzter Track fungiert.
ms.assetid: b0a47303-9e3c-4b78-ac90-c5d8fce2b727
title: Iamtimelinecomp-Schnittstelle (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMTimelineComp
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: 645abbb9c5f61fcfd04e433c3cfc61b926ed403d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365843"
---
# <a name="iamtimelinecomp-interface"></a>Iamtimelinecomp-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die **iamtimelinecomp** -Schnittstelle fügt virtuelle Spuren in einer Komposition in [DirectShow-Bearbeitungs Diensten](directshow-editing-services.md) ein bzw. ruft Sie ab.

Eine Komposition ist eine Auflistung von Ebenen, die als einzelner, zusammengesetzter *Track* fungiert. Beispielsweise fungiert eine Komposition, die zwei Spuren mit einem Übergang zwischen Ihnen enthält, als einzelner Track mit dem vorab zusammengesetzten Übergang. Eine Komposition sollte nur Medien mit einem Typ enthalten (z. b. Audiodaten oder Videos), aber diese Einschränkung wird nicht erzwungen. Ein *virtueller Titel* ist ein beliebiges Objekt, das sich in einer Komposition befinden kann, einschließlich Spuren und anderen Kompositionen.

Die obersten Knoten in der Zeitachse sind *Gruppen*. Gruppen implementieren sowohl die `IAMTimelineComp` -Schnittstelle als auch die [**iamtimelinegroup**](iamtimelinegroup.md) -Schnittstelle.

Um ein Kompositions Objekt zu erstellen, rufen Sie [**iamtimeline:: kreateemptynode**](iamtimeline-createemptynode.md) mit dem Wert Timeline- \_ \_ Haupttyp \_ Composite auf. Sie können den zurückgegebenen [**iamtimelineobj**](iamtimelineobj.md) -Zeiger für die- `IAMTimelineComp` Schnittstelle Abfragen. Weitere Informationen finden Sie [unter Zeitachsen Modell](the-timeline-model.md) und [Erstellen einer Zeitachse](constructing-a-timeline.md).

## <a name="members"></a>Member

Die **iamtimelinecomp** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iamtimelinecomp** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iamtimelinecomp** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                       | BESCHREIBUNG                                                                                                                                               |
|:-----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getgräfin Service Type**](iamtimelinecomp-getcountoftype.md)                     | Ruft rekursiv die Anzahl der Objekte eines angegebenen Typs ab, der in dieser Komposition und allen virtuellen Spuren enthalten ist.<br/>                      |
| [**Getnextvtrack**](iamtimelinecomp-getnextvtrack.md)                       | Ruft den nächsten virtuellen Titel nach einer angegebenen virtuellen Spur ab.<br/>                                                                              |
| [**Getrecursivelayeroftype**](iamtimelinecomp-getrecursivelayeroftype.md)   | Führt eine tiefen erste Reihenfolge der virtuellen Spuren in dieser Komposition aus und ruft die *n*-te virtuelle Spur aus dieser Reihenfolge ab.<br/> |
| [**Getrecursivelayeroftypei**](iamtimelinecomp-getrecursivelayeroftypei.md) | Wird nicht unterstützt.<br/>                                                                                                                                 |
| [**Getvtrack**](iamtimelinecomp-getvtrack.md)                               | Ruft den virtuellen Track mit der angegebenen Priorität ab.<br/>                                                                                         |
| [**Vtrackgetcount**](iamtimelinecomp-vtrackgetcount.md)                     | Ruft die Anzahl der in der Komposition enthaltenen virtuellen Spuren ab.<br/>                                                                           |
| [**Vtrackinsbefore**](iamtimelinecomp-vtrackinsbefore.md)                   | Fügt eine virtuelle Spur mit der angegebenen Priorität in die Komposition ein.<br/>                                                                        |
| [**Vtracktauapprioritäten**](iamtimelinecomp-vtrackswappriorities.md)         | Schaltet die Prioritäts Ebenen von zwei Spuren um.<br/>                                                                                                    |



 

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



 

 
