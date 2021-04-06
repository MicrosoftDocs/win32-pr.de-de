---
title: Arbeiten mit Geräte Konformitäts Vorlagen
description: Arbeiten mit Geräte Konformitäts Vorlagen
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- Profile, Vorlagen für Geräte Konformität
- Profile, Konformitäts Vorlagen
- Codecs, Geräte Konformitäts Vorlagen
- Codecs, Konformitäts Vorlagen
- Geräte Konformitäts Vorlagen, Informationen zu
- Konformitäts Vorlagen
- Vorlagen, Geräte Konformitäts Vorlagen
- Advanced Systems Format (ASF), Geräte Konformitäts Vorlagen
- ASF (Advanced Systems Format), Geräte Konformitäts Vorlagen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104101250"
---
# <a name="working-with-device-conformance-templates"></a>Arbeiten mit Geräte Konformitäts Vorlagen

Aufgrund der großen Flexibilität von ASF-Dateien ist es häufig schwierig, zu bestimmen, ob eine Datei für die Wiedergabe auf einem bestimmten Gerät geeignet ist. Beispielsweise sind Dateien, die für die lokale Wiedergabe auf Desktop Computern geschrieben wurden, nicht optimal für die Verwendung auf handgehaltenen Geräten geeignet. Mit Geräte Konformitäts Vorlagen können Anwendungen schnell den Typ des Wiedergabe Geräts identifizieren, für das eine Datei vorgesehen war. Wenn die Vorlage für die Geräte Konformität nicht mit dem Gerät übereinstimmt, kann die Anwendung den Benutzer darüber informieren, dass die Datei für das Gerät ungeeignet ist. Auf diese Weise kann der Benutzer sicher sein, dass er eine bessere Wiedergabefunktion hat.

Wenn Sie Dateien exklusiv für die Verwendung auf PCs schreiben, sind die Geräte Konformitäts Vorlagen nicht so groß wie beim Erstellen von Profilen. Der Hauptzweck dieser Vorlagen besteht darin sicherzustellen, dass Dateien, die für die Verwendung mit spezieller Hardware erstellt werden, mit einer Vielzahl von Geräten und nicht nur mit einem einzigen Gerät kompatibel sind.

Eine Vorlage für die Geräte Konformität ist eine Behauptung, dass eine ASF-Datei Daten enthält, die in bestimmten Parametern codiert sind. Weitere Informationen zu den Einstellungen, die für die einzelnen Vorlagen geeignet sind, finden Sie unter Geräte Übereinstimmungs- [Vorlagen Parameter](device-conformance-template-parameters.md).

Die folgenden Codecs unterstützen Geräte Konformitäts Vorlagen:

-   Windows Media Video 9
-   Windows Media Audio 9 und höher
-   Windows Media Audio 9 Professional und höher
-   Windows Media Audio 9-Stimme

Sie müssen keine besonderen Schritte ausführen, um die Geräte Konformitäts Vorlagen zu verwenden. Der Codec schreibt automatisch eine Vorlagen Zeichenfolge für jeden entsprechenden Stream in der Datei. Der Codec entscheidet basierend auf den Datenstrom-Konfigurationseinstellungen im Profil, welche Vorlage verwendet werden soll. Es gibt einige Überschneidungen in den Vorlagen Parametern der Geräte Übereinstimmung, sodass Sie eine bestimmte Vorlage anfordern möchten, anstatt dem Codec eine Zuweisung für Sie zu ermöglichen. Sie können angeben, welche Vorlage Sie möchten, indem Sie die \_ Eigenschaft g wszdecodercomplexityangeforderten mit den Methoden der [**iwmpropertyvault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) -Schnittstelle des entsprechenden Datenstrom-Konfigurations Objekts festlegen.

Wenn eine ASF-Datei geschrieben wird, wird die tatsächliche Geräte Konformitäts Vorlage für jeden Stream auf den Wert festgelegt, der vom Codec an den Writer übermittelt wird. Beim Öffnen einer Datei zum lesen können Sie mithilfe der Methoden der [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) -Schnittstelle ermitteln, welcher Vorlage die Streams der Datei entsprechen, um das g \_ wszdeviceconformancetemplate-Attribut auf Streamebene abzurufen. Weitere Informationen zu Attributen finden Sie unter [Arbeiten mit Metadaten](working-with-metadata.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Entwerfen von Profilen**](designing-profiles.md)
</dt> <dt>

[**Parameter für die Geräte Konformitäts Vorlage**](device-conformance-template-parameters.md)
</dt> </dl>

 

 




