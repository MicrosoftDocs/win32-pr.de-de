---
description: Suchen nach Nicht-Win32 PE-Ressourcen
ms.assetid: 12f0b78e-ca85-443a-94ea-6bec5aa40c06
title: Suchen nach Nicht-Win32 PE-Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcf706712b2e1be2dd8fb1598c1404a829251bb24db83db7c7d6deaa87a13d24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147173"
---
# <a name="locating-non-win32-pe-resources"></a>Suchen nach Nicht-Win32 PE-Ressourcen

Um Nicht-Win32 PE-Ressourcen zu suchen, sollte Ihre Anwendung zuerst die [**GetFileMUIPath-Funktion**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath) aufrufen, um die sprachspezifische Ressourcendatei zu suchen, aus der Ressourcen geladen werden sollen. Wenn die Anwendung den Systemspracheinstellungen folgt, muss sie die Funktion mit DEN \_ \_ FÜR dwFlags angegebenen LANGUAGE NAME \| USERNAME USER \_ \_ PREFERRED UI LANGUAGES und für \_ \_ *pwszLanguage* **null** aufrufen.  Wenn die Anwendung anwendungsspezifische Spracheinstellungen verwendet, verwendet sie **GetFileMUIPath,** um zu ermitteln, ob eine sprachspezifische Datei vorhanden ist, indem die Sprache im *pwszLanguage-Parameter* angegeben wird.

Nach dem Aufruf von [**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)muss die Anwendung benutzerdefinierte Funktionen definieren, um das Ressourcenmodul zu laden und bestimmte Ressourcen daraus zu laden. Wenn Sie beispielsweise eine .txt oder .xml Ressourcendatei verwenden, muss die Anwendung einen TXT- oder XML-Parser verwenden, um die Datei zu laden und dann den Inhalt der Datei für jede erforderliche Ressource zu analysieren.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Verwenden von mehrsprachige Benutzeroberfläche](using-multilingual-user-interface.md)
</dt> <dt>

[**GetFileMUIPath**](/windows/desktop/api/Winnls/nf-winnls-getfilemuipath)
</dt> </dl>

 

 



