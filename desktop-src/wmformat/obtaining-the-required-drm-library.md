---
title: Abrufen der erforderlichen DRM-Bibliothek
description: Abrufen der erforderlichen DRM-Bibliothek
ms.assetid: 7bd13b77-439e-40cf-99e8-b359247da74d
keywords:
- Windows Media-Format-SDK, Abrufen erforderlicher DRM-Bibliotheken
- Advanced Systems Format (ASF), Abrufen erforderlicher DRM-Bibliotheken
- ASF (Advanced Systems Format), Abrufen erforderlicher DRM-Bibliotheken
- Digital Rights Management (DRM), Abrufen erforderlicher Bibliotheken
- DRM (Digital Rights Management), Abrufen erforderlicher Bibliotheken
- Digital Rights Management (DRM), Buildinformationen
- DRM (Digital Rights Management), Buildinformationen
- Digital Rights Management (DRM), Debuginformationen
- DRM (Digital Rights Management), Debuginformationen
- Debugging von DRM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f5c124c1e7edf0bba736b9dd392e852aac97e96
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/09/2020
ms.locfileid: "104391150"
---
# <a name="obtaining-the-required-drm-library"></a>Abrufen der erforderlichen DRM-Bibliothek

Zum Erstellen oder Wiedergeben von DRM-geschützten digitalen Mediendateien muss Ihre Anwendung mit einer statischen Bibliothek verknüpft werden, die von Microsoft in binärer Form bereitgestellt wird. Diese Bibliothek wird manchmal als Stub-Bibliothek oder "stublib" bezeichnet und identifiziert Ihre Anwendung eindeutig.

In dieser Dokumentation wird die DRM-Bibliothek als "wmstubdrm. lib" bezeichnet. Der Name der Bibliothek, die Sie erhalten, enthält eine identifizierende Nummer. Um diese Bibliothek zu erhalten, müssen Sie einen Lizenzvertrag bei Microsoft signieren. Die Bedingungen der Vereinbarung können sich je nachdem, ob Sie eine Evaluierungslizenz oder eine Produktionslizenz anfordern, unterscheiden. Weitere Informationen zum DRM-Lizenzierungsprozess finden Sie im Windows Media Licensing-Formular auf der [Microsoft-Website](https://www.microsoft.com/licensing/default).

Die Bibliothek, die Sie erhalten, verfügt über eine DRM-Sicherheitsstufe, die von dem Typ des Lizenzvertrags abhängt, den Sie eingeben. Eine DRM-Lizenz kann Anwendungen mit DRM-Komponenten unter einer bestimmten Sicherheitsstufe einschränken, indem Sie auf den Dateiinhalt zugreift. Diese Sicherheitsstufe ist nicht identisch mit der DRM-Individualisierungs Ebene, und Sie bezieht sich nicht auf einen der numerischen Werte der Ausgabe Schutz Ebenen (opls). In der folgenden Tabelle sind Beispiele für DRM-Sicherheitsstufen für verschiedene Player und portable Geräte aufgeführt.



| Sicherheitsstufe | Player und portable Geräte                                                                                                                                                                                                                                                                                                   | Beispiel                                                                                                                                                                                          |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 150            | Geräte, die Windows Media DRM nicht unterstützen. Der DRM-Schutz wird entfernt, wenn Inhalte auf ein solches Gerät übertragen werden.                                                                                                                                                                                                         | Geräte, die Windows Media-basierte Inhalte, aber nicht geschützte Inhalte unterstützen                                                                                                                       |
| 1\.000          | Player Anwendungen basierend auf dem Windows Media-Format 9,5 SDK oder früher, die keine zusätzlichen Anforderungen für Level 2000 erfüllen. Geräte, die auf dem Windows Media Portable-Gerät DRM v1 basieren.<br/> Geräte, die auf Windows CE 4,2 und höher basieren.<br/>                                                                       | Windows Media Player 6,4, Windows Media Player 7portable Mediengeräte, die Windows Media Portable Geräte DRM v1 unterstützen.<br/>                                                             |
| 2\.000          | Player-Anwendungen, die auf dem Windows Media-Format 9 oder höher basieren und eine strengere Sammlung von Richtlinien für den Inhalts Schutz befolgen als Anwendungen auf Ebene 1000. Geräte, die auf Windows Media DRM 10 für tragbare Geräte basieren.<br/> Geräte, die auf Windows Media DRM 10 für Netzwerkgeräte basieren<br/> | Windows Media Player 9-Serie und lateral portable-Mediengeräte, die Windows Media DRM 10 für tragbare Geräte unterstützen<br/> Portable Media Center-Geräte, die auf Windows Mobile basieren<br/> |



 

## <a name="build-and-debugging-information"></a>Build-und Debuginformationen

Wenn Sie einen Link zu "wmstubdrm. lib" herstellen, dürfen Sie nicht mit "Wmvcore. lib" verknüpfen. Die DRM-Komponente funktioniert nicht ordnungsgemäß, wenn die Anwendung mit beiden Bibliotheken verknüpft ist.

Ein Benutzer Haltepunkt in der DRM-Komponente verhindert, dass sowohl die Debug-als auch die Releaseversion der Anwendungen auf geschützte Inhalte zugreifen, wenn Sie im Debugger ausgeführt werden. Zum Beheben von Problemen mit DRM-bezogenen Funktionen in Ihrer Anwendung müssen Sie eigene Ablauf Verfolgungs Routinen schreiben, mit denen Informationen wie **HRESULT** -Werte an einem Speicherort wie z. b. einer Protokolldatei gespeichert werden.

Wenn Sie versuchen, eine Releaseversion einer Anwendung auf einem System mit einer Debugversion der SDK-Bits (oder umgekehrt) auszuführen, treten beim Wiedergeben von DRM-Inhalt der Version 7 Heap Fehler auf. Stellen Sie sicher, dass Sie debugginganwendungen über Debug SDK Bits ausführen und Anwendungen über releasebits freigeben. Das gleiche Problem tritt auf, wenn Sie eine Debugversion des SDK mit einer individualisierten DRM-Komponente ausführen (bei der es sich immer um einen Releasebuild handelt).

**Hinweise** DRM wird von der x64-basierten Version dieses SDK nicht unterstützt.

Die wmstubdrm. lib-Dateien, die dem SDK für den Windows Media-Format 9,5 zugeordnet sind, können nur mit den Komponenten von Microsoft Visual Studio .NET 2003 verwendet werden. Wenn Sie eine ältere Version der Stub-Bibliothek verwenden, gibt es keine neuen Einschränkungen für deren Verwendung.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Aktivieren DRM-Unterstützung**](enabling-drm-support.md)
</dt> </dl>

 

 





