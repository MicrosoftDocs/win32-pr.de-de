---
description: Zeigt die Member der cxapoparametersbase-Klasse an.
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: Cxapoparametersbase-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e225d1628408b5d5472bed8c3060f714bb7b0ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373145"
---
# <a name="cxapoparametersbase-members"></a>Cxapoparametersbase-Member

Zeigt die Member der [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) -Klasse an.

## <a name="public-constructors"></a>Öffentliche Konstruktoren



|                                                    |                                                                         |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**Cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | Erstellt ein [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) -Objekt. |



 

## <a name="public-methods"></a>Öffentliche Methoden



|                                                                                                                              |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adressf**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                                         | Inkremente den Verweis Zähler des xapo-Objekts.<br/>                                                                                                         |
| [**Beginprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | Gibt die aktuellen Prozessparameter zurück. <br/>                                                                                                              |
| [**Calcinputframes**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                           | Gibt die Anzahl der Eingabe Frames zurück, die erforderlich sind, um die angegebene Anzahl von Ausgabe Frames zu generieren.<br/>                                                            |
| [**Calcoutputframes**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                         | Gibt die Anzahl der Ausgabe Frames zurück, die erforderlich sind, um die angegebene Anzahl von Eingabe Frames zu generieren.<br/>                                                            |
| [**Endprocess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | Benachrichtigt [**cxapoparametersbase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) , dass der xapo-Zugriff auf die aktuellen Prozessparameter abgeschlossen hat. <br/>                     |
| [**GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (von [**ixapoparameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)geerbt) | Ruft Effekt spezifische Parameter ab. <br/>                                                                                                                     |
| [**Getregistrationproperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)       | Gibt die Registrierungs Eigenschaften eines xapo zurück.<br/>                                                                                                       |
| [**Initialisieren**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                                     | Führt eine beliebige Wirkungs spezifische Initialisierung aus.<br/>                                                                                                          |
| [**Isinputformatsupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)             | Fragt ab, ob ein bestimmtes Eingabeformat für ein bestimmtes Ausgabeformat unterstützt wird.<br/>                                                                            |
| [**Isoutputformatsupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)           | Fragt ab, ob ein bestimmtes Ausgabeformat für ein bestimmtes Eingabeformat unterstützt wird.<br/>                                                                            |
| [**Lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                             | Benachrichtigt xapo von streamformaten, dass der [**Prozess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) angegeben wird.<br/>                                                             |
| [**Onsetparameters**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | Wird von [**ixapoparameters:: SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) aufgerufen, um eine benutzerdefinierte Parameter Validierung zuzulassen. <br/>          |
| [**Parameterschge**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | Gibt an, ob [**ixapoparameters:: SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) seit dem letzten Verarbeitungs Durchlauf aufgerufen wurde. <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (geerbt von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                         | Ruft den angeforderten Schnittstellen Zeiger ab, wenn er vom xapo unterstützt wird.<br/>                                                                                    |
| [**Release**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (geerbt von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                       | Dekremente den Verweis Zähler des xapo-Objekts und löscht das-Objekt, wenn der Verweis Zähler auf 0 (null) fällt.<br/>                                             |
| [**Reset**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                                               | Gibt das-Objekt in den Zustand zurück, in dem es sich unmittelbar nach dem Aufruf von [**lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) befand.<br/>                             |
| [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (von [**ixapoparameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)geerbt) | Legt Effekte spezifische Parameter fest.<br/>                                                                                                                      |
| [**Unlockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                         | Gegenteil von lockforprocess: während der [**lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) zugeordnete Variablen sollte in dieser Methode die Zuordnung aufgehoben werden.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cxapoparametersbase-Klasse**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
