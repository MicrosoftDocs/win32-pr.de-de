---
title: Konfigurieren von Dateneinheitserweiterung en
description: Konfigurieren von Dateneinheitserweiterung en
ms.assetid: 5dc0a596-68ae-409a-9abc-15ca507d6ec7
keywords:
- Streams, Konfigurieren von Dateneinheiten Erweiterungen
- Streams, Dateneinheiten Erweiterungen
- Erweiterungen für Dateneinheiten, konfigurieren
- Profile, Dateneinheiten Erweiterungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc7e6794b95128d180bc3922f9bf03a15a2749df
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/21/2020
ms.locfileid: "103724046"
---
# <a name="configuring-data-unit-extensions"></a>Konfigurieren von Dateneinheitserweiterung en

In ASF-Dateien geschriebene Beispiele können neben den Medien Beispielen selbst zusätzliche Informationen enthalten. Diese Informationen sind unter Verwendung von Dateneinheiten Erweiterungen enthalten. Weitere Informationen zu Dateneinheiten Erweiterungen finden Sie unter [Dateneinheiten Erweiterungen](data-unit-extensions.md).

Um dateneinheits Erweiterungen zu verwenden, müssen Sie den Stream im Profil so konfigurieren, dass Sie akzeptiert werden. Führen Sie die folgenden Schritte aus, um eine Dateneinheiten Erweiterung für einen Stream zu konfigurieren.

1.  Abrufen eines Zeigers auf die [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) -Schnittstelle durch Aufrufen der **QueryInterface** -Methode von [**iwmstreamconfig**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig).
2.  Aufrufen von [**IWMStreamConfig2:: adddataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) zum Registrieren eines Typs der Dateneinheiten Erweiterung für den Datenstrom.

Durch Aufrufen von [**IWMStreamConfig2:: getdataunitextensioncount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextensioncount) können Sie alle zurzeit für einen Stream registrierten dateieinheits-Erweiterungs Typen überprüfen, um die Anzahl der registrierten Dateneinheiten-Erweiterungs Typen abzurufen. Anschließend können Sie alle Typen mithilfe von Aufrufen von [**IWMStreamConfig2:: getdataunitextension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-getdataunitextension) für jede Schleife durchlaufen.

Dateneinheiten Erweiterungen wird eine Größe zugewiesen, wenn Sie für einen Stream konfiguriert wird. Viele Dateneinheiten Erweiterungs Systeme verwenden Daten, bei denen es sich um eine konstante Größe handelt (normalerweise eine Struktur). Sie können jedoch auch die Größe Ihrer dateneinheits Erweiterungen so konfigurieren, dass Sie eine Variable Größe aufweisen, indem Sie die Größe auf "0xFFFF" festlegen. Jede dateneinheits Erweiterung, die zur Codierungs Zeit zugewiesen wird, kann dann eine beliebige Größe zwischen 1 Byte und 65534 Bytes aufweisen. Dateneinheiten Erweiterungen mit variabler Größen Bezeichnung werden auch als dynamische Dateneinheiten Erweiterungen bezeichnet.

Der Vorteil der Verwendung dynamischer dateneinheits Erweiterungen besteht darin, dass Sie bei Bedarf Erweiterungs Daten anfügen können. Wenn Sie eine Dateneinheiten Erweiterung mit einer festgelegten Größe definieren, muss jede Stichprobe für den Stream Erweiterungs Daten dieser Größe enthalten, auch wenn Sie über keine Daten für einige Beispiele verfügen. Mit dynamischen Dateneinheiten Erweiterungen können Sie Dateneinheiten Erweiterungen aus einigen Beispielen weglassen, wodurch Speicherplatz gespart und die Bandbreitenanforderungen reduziert werden. Wenn die Größe von Dateneinheiten Erweiterungen jedoch variabel ist, kann das Lese Objekt die empfangenen Erweiterungs Daten mit einer statischen Größe nicht überprüfen. Sie müssen überprüfen, ob die von Ihnen empfangenen Erweiterungs Daten gültig sind und nicht die böswillige Verzerrung des Bitstreams.

Einzelne Dateneinheiten Erweiterungen müssen mithilfe der [**INSSBuffer3:: SetProperty**](/previous-versions/windows/desktop/api/Wmsbuffer/nf-wmsbuffer-inssbuffer3-setproperty) -Methode für-Beispiele festgelegt werden. Weitere Informationen finden Sie unter [Festlegen von Dateneinheiten Erweiterungen](setting-data-unit-extensions.md).

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Konfigurieren von Streams**](configuring-streams.md)
</dt> </dl>

 

 




