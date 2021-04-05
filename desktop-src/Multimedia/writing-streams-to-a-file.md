---
title: Schreiben von Datenströmen in eine Datei
description: Schreiben von Datenströmen in eine Datei
ms.assetid: a3766f8c-aaa6-4fc5-a306-54aee71018f1
keywords:
- Avifilekreatestream-Funktion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 370df08534bbdde870f6d28c828d47935abd80db
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "103725544"
---
# <a name="writing-streams-to-a-file"></a>Schreiben von Datenströmen in eine Datei

Sie können auch eine Datei mit Datenströmen erstellen, indem Sie einen neuen Datenstrom in eine Datei schreiben.

Sie können einen neuen Stream in einer neuen oder vorhandenen Datei erstellen, indem Sie die [**avifilekreatestream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) -Funktion verwenden. Diese Funktion definiert einen neuen Stream gemäß den in einer [**AVISTREAMINFO**](/windows/desktop/api/Vfw/ns-vfw-avistreaminfoa) -Struktur beschriebenen Merkmalen, erstellt eine streamschnittstelle für den neuen Stream, erhöht den Verweis Zähler des Streams und gibt die Adresse des Stream-Schnittstellen Zeigers zurück.

Bevor Sie den Inhalt des Streams schreiben, müssen Sie das Streamformat angeben. Sie können das Streamformat mithilfe der [**avistreamsetformat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) -Funktion festlegen. Wenn Sie das Format eines Videostreams festlegen, müssen Sie diese Funktion mit einer [**BitmapInfo**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfo) -Struktur bereitstellen, die die entsprechenden Informationen enthält. Wenn Sie das Format eines Audiostreams festlegen, müssen Sie eine [**Waveformat**](/windows/win32/api/mmreg/ns-mmreg-waveformat) -oder [**WaveFormatEx**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) -Struktur mit den entsprechenden Informationen angeben. Die Informationen, die Sie für die Funktion für andere Streamtypen angeben müssen, hängen vom Streamtyp und vom Datenstrom Handler ab.

Sie können den Multimedia-Inhalt in einen Stream schreiben, indem Sie die [**AVIStreamWrite**](/windows/desktop/api/Vfw/nf-vfw-avistreamwrite) -Funktion verwenden. Diese Funktion kopiert Rohdaten aus einem von der Anwendung bereitgestellten Puffer in den angegebenen Stream. Der Standard-AVI-Datei Handler fügt Informationen an das Ende eines Streams an. Der standardmäßige Wave-Handler kann Wellenform-Audiodaten in einen Stream und am Ende eines Streams schreiben.

Sie können zusätzliche Informationen über die Datei oder den Stream schreiben, die nicht in der [**avifileanatestream**](/windows/desktop/api/Vfw/nf-vfw-avifilecreatestream) -oder [**avistreamsetformat**](/windows/desktop/api/Vfw/nf-vfw-avistreamsetformat) -Funktion enthalten ist, indem Sie die Funktionen [**avifileschreitedata**](/windows/desktop/api/Vfw/nf-vfw-avifilewritedata) und [**avistreamschreitedata**](/windows/desktop/api/Vfw/nf-vfw-avistreamwritedata) verwenden. Mithilfe von **avifilewrite-Data** können Sie Daten aufzeichnen, die für die gesamte Datei (z. b. Copyright Informationen und Änderungs Verlauf) gelten. Sie können Datenstrom spezifische Informationen (z. b. Komprimierungs-und Dekomprimierungs Einstellungen) mithilfe von **avistreamschreitedata** aufzeichnen. Die ergänzenden Informationen werden in separaten Blöcken in der Datei gespeichert.

Sie können den Datenstrom schließen, nachdem Sie mit der [**avistreamrelease**](/windows/desktop/api/Vfw/nf-vfw-avistreamrelease) -Funktion das Schreiben in den neuen Stream abgeschlossen haben. Mit dieser Funktion werden Puffer gelöscht, die zum Aufzeichnen der Streamdaten verwendet werden, und alle unvollständigen Datenblöcke in der Datei werden abgeschlossen und geschlossen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Streamoperationen](stream-operations.md)
</dt> </dl>

 

 