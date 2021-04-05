---
title: Iwmdrmindividualizationstatus-Schnittstelle
description: Die iwmdrmindividualizationstatus-Schnittstelle ermöglicht das Abrufen erweiterter Statusinformationen über den Fortschritt der Individual alisierung. Diese Schnittstelle wird mit mewmdrmindividualizationprogress-Ereignissen geliefert.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Iwmdrmindividualizationstatus-Schnittstelle Windows Media-Format
- Iwmdrmindividualizationstatus Interface Windows Media-Format, beschrieben
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 19a369bf9b70d9a43af8a48f13f1b8bbb87525b1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948991"
---
# <a name="iwmdrmindividualizationstatus-interface"></a>Iwmdrmindividualizationstatus-Schnittstelle

Die **iwmdrmindividualizationstatus** -Schnittstelle ermöglicht das Abrufen erweiterter Statusinformationen über den Fortschritt der Individual alisierung.

Diese Schnittstelle wird mit mewmdrmindividualizationprogress-Ereignissen geliefert. Viele derartige Ereignisse werden zwischen einem Aufruf von [**iwmdrmsecurity::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) und dem Abschluss des Individualisierungs Prozesses generiert, der durch die Generierung eines **mewmdrmindividualizationabgeschlossene** -Ereignisses signalisiert wird.

Wenn Sie einen Zeiger auf eine Instanz der **iwmdrmindividualizationstatus** -Schnittstelle abrufen möchten, müssen Sie zuerst die **imfmediaevent:: GetValue** -Methode des Fortschritts Ereignisses aufrufen. Der Wert, den Sie aus dem Ereignis abrufen, ist ein Zeiger auf die **IUnknown** -Schnittstelle des Objekts, das die **iwmdrmindividualizationstatus** -Schnittstelle implementiert.

## <a name="members"></a>Member

Die **iwmdrmindividualizationstatus** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Iwmdrmindividualizationstatus** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **iwmdrmindividualizationstatus** -Schnittstelle verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetStatus**](iwmdrmindividualizationstatus-getstatus.md) | Ruft ausführliche Informationen zur Individualisierung ab.<br/> |



 

## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Schnittstellen**](drm-interfaces.md)
</dt> </dl>

 

