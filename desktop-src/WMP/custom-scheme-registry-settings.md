---
title: Benutzerdefinierte Schemaregistrierungs Einstellungen
description: Benutzerdefinierte Schemaregistrierungs Einstellungen
ms.assetid: ded2b492-7755-4ba5-87cf-720a79ec79de
keywords:
- Windows Media Player,Registrierungseinstellungen für benutzerdefinierte Schemas
- Windows Media Player,Schemas
- Windows Media Player, Registrierung
- Registrierung, benutzerdefinierte Schemaeinstellungen
- Registrierung,Schemas
- registry,settings for Windows Media Player
- Schemas
- Registrierungseinstellungen für benutzerdefinierte Schemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af1f20b69570a18d256049bb0e785099e43b091d080e4f9f65e62655c3103d68
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117750393"
---
# <a name="custom-scheme-registry-settings"></a>Benutzerdefinierte Schemaregistrierungs Einstellungen

Schemas sind benutzerdefinierte Protokolle. Windows Media Player verwaltet eine Liste von Schemas in der Registrierung auf dem Computer des Benutzers. Wenn der Benutzer versucht, eine digitale Mediendatei wieder zu spielen, überprüft der Player zuerst, ob das Windows Media Format SDK das Schema unterstützt. Ist dies nicht der Der Player überprüft das Schema mit der Liste in der Registrierung. Wenn eine Übereinstimmung gefunden wird, überprüft der Player dann einen  Wert, der angibt, welche zugrunde liegende Technologie oder Runtime (z. B. Microsoft DirectShow oder das Windows Media Format SDK) verwendet werden kann, um die Datei wiedergibt. Wenn keine Übereinstimmung gefunden wird, zeigt der Player dem Benutzer ein Warndialogfeld an, in dem der Benutzer aufgefordert wird, die Berechtigung zum Wieder geben der Datei zu erteilen. Wenn Sie digitale Mediendateien mithilfe eines benutzerdefinierten Protokollschemas streamen, können Sie verhindern, dass diese Warnung auf dem Computer des Benutzers angezeigt wird, indem Sie das Schema registrieren und einen Wert für die Laufzeit angeben.

Die Liste der Schemas wird als Satz von Registrierungsschlüsseln verwaltet, die mit den registrierten Schemas übereinstimmen, ohne den Doppelpunkt und die beiden Schrägstriche (://). Der Schlüssel für das Schema wmhtml://, das zum Streamen von Rich Media verwendet wird, hat beispielsweise den Namen "wmhtml". Für den lokalen Computer und jeden Benutzer wird eine separate Liste verwaltet. Für den lokalen Computer sind die Schemaschlüssel Unterschlüssel des folgenden Registrierungsschlüssels:

**HKEY \_ LOCAL MACHINE Software Microsoft Multimedia \_ \\ \\ \\ \\ WMPlayer-Schemas \\\\**

Der Schlüssel für das Schema wmhtml:// für den lokalen Computer ist beispielsweise:

**HKEY \_ LOCAL MACHINE Software Microsoft Multimedia \_ \\ \\ \\ \\ WMPlayer Schemes \\ \\ wmhtml**

Um Werte in diesem Schlüssel zu ändern oder einen neuen Unterschlüssel zu erstellen, muss der aktuelle Benutzer administrator für den Computer sein.

Für einzelne Benutzer sind die Schemaschlüssel Unterschlüssel des folgenden Registrierungsschlüssels:

**HKEY \_ CURRENT USER Software Microsoft \_ \\ \\ \\ MediaPlayer \\ \\ Player-Schemas\\**

Der Schlüssel für das Schema wmhtml:// für den aktuellen Benutzer ist beispielsweise:

**HKEY \_ CURRENT USER Software Microsoft \_ \\ \\ \\ MediaPlayer Player Schemes \\ \\ \\ wmhtml**

Bei der Überprüfung auf registrierte Schemas überprüft der Player zuerst die Werte in **HKEY \_ LOCAL \_ MACHINE.** Wenn keine Werte für das aktuelle Schema gefunden werden, überprüft der Player als Nächstes die Werte in **HKEY \_ CURRENT \_ USER**. Wenn keines für das aktuelle Schema gefunden wird, zeigt der Player dem Benutzer die Warnung an.

Jeder Schemaunterschlüssel kann einen der folgenden möglichen Werte für *Runtime enthalten.*



| Wert | Beschreibung                                |
|-------|--------------------------------------------|
| 6     | Rendern sie mit Windows Medienformat-SDK. |
| 7     | Rendern mitHilfe von Microsoft DirectShow.         |



 

Das Ändern *des Laufzeitwerts* für ein Schema, das vom Windows Media Format SDK unterstützt wird, hat keine Auswirkungen. Der Player verwendet immer das Windows Media Format SDK als Laufzeit für Schemas, die das Windows Media Format SDK unterstützt. Dieser Registrierungswert ist so konzipiert, dass die Laufzeitkonfiguration für benutzerdefinierte Schemas zulässig ist.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Registrierungseinstellungen**](registry-settings.md)
</dt> </dl>

 

 




