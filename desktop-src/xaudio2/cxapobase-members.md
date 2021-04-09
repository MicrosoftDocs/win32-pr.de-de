---
description: Zeigt die Member der cxapobase-Klasse an.
ms.assetid: 0791888B-7215-475B-95C8-B558A1E57783
title: Cxapobase-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9ab63cf7e8ac6e4d0fa14ec412b53682aff2ba5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042565"
---
# <a name="cxapobase-members"></a>Cxapobase-Member

Zeigt die Member der [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) -Klasse an.

## <a name="public-constructors"></a>Öffentliche Konstruktoren



|                                |                                                     |
|--------------------------------|-----------------------------------------------------|
| [**Cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) | Erstellt ein [**cxapobase**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase) -Objekt. |



 

## <a name="public-methods"></a>Öffentliche Methoden



|                                                                                                                        |                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Adressf**](/previous-versions/windows/desktop/legacy/ee418448(v=vs.85)) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                                   | Inkremente den Verweis Zähler des xapo-Objekts.<br/>                                                                                                         |
| [**Calcinputframes**](/windows/win32/api/xapo/nf-xapo-ixapo-calcinputframes) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                     | Gibt die Anzahl der Eingabe Frames zurück, die erforderlich sind, um die angegebene Anzahl von Ausgabe Frames zu generieren.<br/>                                                            |
| [**Calcoutputframes**](/windows/win32/api/xapo/nf-xapo-ixapo-calcoutputframes) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                   | Gibt die Anzahl der Ausgabe Frames zurück, die erforderlich sind, um die angegebene Anzahl von Eingabe Frames zu generieren.<br/>                                                            |
| [**Getregistrationproperties**](/windows/win32/api/xapo/nf-xapo-ixapo-getregistrationproperties) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt) | Gibt die Registrierungs Eigenschaften eines xapo zurück.<br/>                                                                                                       |
| [**Initialisieren**](/windows/win32/api/xapo/nf-xapo-ixapo-initialize) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                               | Führt eine beliebige Wirkungs spezifische Initialisierung aus.<br/>                                                                                                          |
| [**Isinputformatsupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isinputformatsupported) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)       | Fragt ab, ob ein bestimmtes Eingabeformat für ein bestimmtes Ausgabeformat unterstützt wird.<br/>                                                                            |
| [**Isoutputformatsupported**](/windows/win32/api/xapo/nf-xapo-ixapo-isoutputformatsupported) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)     | Fragt ab, ob ein bestimmtes Ausgabeformat für ein bestimmtes Eingabeformat unterstützt wird.<br/>                                                                            |
| [**Lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                       | Benachrichtigt xapo von streamformaten, dass der [**Prozess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) angegeben wird.<br/>                                                             |
| [**QueryInterface**](/previous-versions/windows/desktop/legacy/ee418457(v=vs.85)) (geerbt von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                   | Ruft den angeforderten Schnittstellen Zeiger ab, wenn er vom xapo unterstützt wird.<br/>                                                                                    |
| [**Release**](/previous-versions/windows/desktop/legacy/ee418458(v=vs.85)) (geerbt von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo))                                 | Dekremente den Verweis Zähler des xapo-Objekts und löscht das-Objekt, wenn der Verweis Zähler auf 0 (null) fällt.<br/>                                             |
| [**Reset**](/windows/win32/api/xapo/nf-xapo-ixapo-reset) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                                         | Gibt das-Objekt in den Zustand zurück, in dem es sich unmittelbar nach dem Aufruf von [**lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) befand.<br/>                             |
| [**Unlockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-unlockforprocess) (von [**ixapo**](/windows/desktop/api/XAPO/nn-xapo-ixapo)geerbt)                   | Gegenteil von lockforprocess: während der [**lockforprocess**](/windows/win32/api/xapo/nf-xapo-ixapo-lockforprocess) zugeordnete Variablen sollte in dieser Methode die Zuordnung aufgehoben werden.<br/> |



 

## <a name="protected-methods"></a>Geschützte Methoden



|                                                                                          |                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Getregistrationpropertiesinternal**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-getregistrationpropertiesinternal) | Gibt einen Zeiger auf die [**xapo- \_ Registrierungs \_ Eigenschaften**](/windows/desktop/api/xapo/ns-xapo-xapo_registration_properties)S-Struktur zurück, die die Registrierungs Eigenschaften enthält, mit denen der xapo erstellt wurde.<br/> |
| [**IsLocked**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-islocked)                                                   | Überprüft, ob xapo gesperrt ist.<br/>                                                                                                                                                |
| Long m \_ lreferencecount<br/>                                                       | Der com-Verweis Zähler des xapo-Objekts.<br/>                                                                                                                                       |
| [**Processthru**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-processthru)                                             | Wird von einer [**ixapo::P rocess**](/windows/win32/api/xapo/nf-xapo-ixapo-process) -Implementierung aufgerufen, wenn ein xapo für die Verarbeitung durch den Prozess deaktiviert wird.<br/>                                                  |
| [**Validateformatdefault**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatdefault)                         | Überprüft, ob ein Audioformat innerhalb der Standard Bereiche liegt, die unterstützt werden.<br/>                                                                                                     |
| [**Validateformatpair**](/windows/win32/api/xapobase/nf-xapobase-cxapobase-validateformatpair)                               | Überprüft, ob eine Eingabe-und Ausgabeformat Paar-Konfiguration in Bezug auf die xapo-Eigenschaftenflags unterstützt wird.<br/>                                                            |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Cxapobase-Klasse**](/windows/desktop/api/XAPOBase/nl-xapobase-cxapobase)
</dt> </dl>

 

 
