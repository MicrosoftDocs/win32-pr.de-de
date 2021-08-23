---
description: Zeigt die Member der CXAPOParametersBase-Klasse an.
ms.assetid: C2113358-07DE-426E-AF26-BD8ED9902192
title: CXAPOParametersBase-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ededac8054229cffa7799ced71653ab19cacf74f705e77163556cc5b60b7655d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119770840"
---
# <a name="cxapoparametersbase-members"></a>CXAPOParametersBase-Member

Zeigt die Member der [**CXAPOParametersBase-Klasse**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) an.

## <a name="public-constructors"></a>Öffentliche Konstruktoren



|    Konstruktor                                                |     BESCHREIBUNG                                                                    |
|----------------------------------------------------|-------------------------------------------------------------------------|
| [**CXAPOParametersBase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) | Erstellt ein [**CXAPOParametersBase-Objekt.**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) |



 

## <a name="public-methods"></a>Öffentliche Methoden



|        Methode                                                                                                                      |     Beschreibung                                                                                                                                                             |
|------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddRef**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                         | Erhöht den Verweiszähler des XAPO-Objekts.<br/>                                                                                                         |
| [**BeginProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-beginprocess)                                                                     | Gibt die aktuellen Prozessparameter zurück. <br/>                                                                                                              |
| [**CalcInputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                           | Gibt die Anzahl der Eingabeframes zurück, die zum Generieren der angegebenen Anzahl von Ausgabeframes erforderlich sind.<br/>                                                            |
| [**CalcOutputFrames**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                         | Gibt die Anzahl der Ausgabeframes zurück, die zum Generieren der angegebenen Anzahl von Eingabeframes erforderlich sind.<br/>                                                            |
| [**EndProcess**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-endprocess)                                                                         | Benachrichtigt [**CXAPOParametersBase,**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase) dass das XAPO den Zugriff auf die aktuellen Prozessparameter abgeschlossen hat. <br/>                     |
| [**GetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-getparameters) (geerbt von [**IXAPOParameters**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters)) | Ruft effektspezifische Parameter ab. <br/>                                                                                                                     |
| [**GetRegistrationProperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)       | Gibt die Registrierungseigenschaften eines XAPO zurück.<br/>                                                                                                       |
| [**Initialisieren**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                     | Führt eine beliebige effektspezifische Initialisierung aus.<br/>                                                                                                          |
| [**IsInputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)             | Fragt ab, ob ein bestimmtes Eingabeformat für ein bestimmtes Ausgabeformat unterstützt wird.<br/>                                                                            |
| [**IsOutputFormatSupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)           | Fragt ab, ob ein bestimmtes Ausgabeformat für ein bestimmtes Eingabeformat unterstützt wird.<br/>                                                                            |
| [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                             | Benachrichtigt XAPO über stream formats [**Process**](/windows/win32/api/xapo/nf-xapo-ixapo-process) wird angegeben.<br/>                                                             |
| [**OnSetParameters**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-onsetparameters)                                                               | Wird von [**IXAPOParameters::SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) aufgerufen, um die Validierung benutzerdefinierter Parameter zu ermöglichen. <br/>          |
| [**ParametersChanged**](/windows/win32/api/xapobase/nf-xapobase-cxapoparametersbase-parameterschanged)                                                           | Gibt an, ob [**IXAPOParameters::SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) seit dem letzten Verarbeitungsdurchlauf aufgerufen wurde. <br/>       |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                         | Ruft den angeforderten Schnittstellenzeiger ab, wenn er vom XAPO unterstützt wird.<br/>                                                                                    |
| [**Release**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                       | Dekrementiert den Verweiszähler des XAPO-Objekts und löscht das Objekt, wenn der Verweiszähler auf 0 (null) fällt.<br/>                                             |
| [**Reset**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                                               | Gibt das -Objekt in den Zustand zurück, in dem es sich unmittelbar nach dem Aufruf von [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) befand.<br/>                             |
| [**SetParameters**](/windows/win32/api/xapo/nf-xapo-ixapoparameters-setparameters) (geerbt von [**IXAPOParameters)**](/windows/desktop/api/XAPO/nn-xapo-ixapoparameters) | Legt effektspezifische Parameter fest.<br/>                                                                                                                      |
| [**UnlockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (geerbt von [**IXAPO)**](/windows/desktop/api/XAPO/nn-xapo-ixapo)                         | Gegenüber von LockForProcess: Variablen, die während [**LockForProcess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) zugeordnet werden, sollten in dieser Methode aufgehoben werden.<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**CXAPOParametersBase-Klasse**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapoparametersbase)
</dt> </dl>

 

 
