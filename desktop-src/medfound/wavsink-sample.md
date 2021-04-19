---
description: Beispiel für wavsink
ms.assetid: 9e1af25f-d55c-45db-8c76-abf814e16700
title: Beispiel für wavsink
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e96ecca551b6ea3e6837f211f0afcb34818d635
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359999"
---
# <a name="wavsink-sample"></a>Beispiel für wavsink

Zeigt, wie eine benutzerdefinierte Medien Senke in Microsoft Media Foundation implementiert wird. Das Beispiel implementiert eine Archive-Senke, die unkomprimierte PCM-Audiodaten in eine WAV-Datei schreibt.

## <a name="apis-demonstrated"></a>Gezeigte APIs

In diesem Beispiel werden die folgenden Media Foundation Schnittstellen veranschaulicht:

-   [**IMF-staatink**](/windows/desktop/api/mfidl/nn-mfidl-imfclockstatesink)
-   [**Imffinalizablemediasink**](/windows/desktop/api/mfidl/nn-mfidl-imffinalizablemediasink)
-   [**Imfmediasink**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)
-   [**IMF mediatypeer Handler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler)
-   [**IMF-Senke**](/windows/desktop/api/mfidl/nn-mfidl-imfstreamsink)

## <a name="usage"></a>Verbrauch

Das Beispiel wavsink enthält zwei Visual Studio-Projekte:

-   Wavsink. vcproj erstellt eine statische Bibliothek, die die Medien Senke-Implementierung enthält.
-   "Writewavfile. vcproj" erstellt eine Konsolenanwendung, die die Medien Senke verwendet, um eine WAV-Datei zu erstellen. Diese Anwendung ist mit der Bibliothek verknüpft, die vom wavsink-Projekt erstellt wurde.

## <a name="requirements"></a>Anforderungen



| Produkt                                                        | Version   |
|----------------------------------------------------------------|-----------|
| [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx) | Windows 7 |



 

## <a name="downloading-the-sample"></a>Herunterladen des Beispiels

Dieses Beispiel ist im [GitHub-Repository für klassische Windows-Beispiele](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/multimedia/mediafoundation/wavsink)verfügbar.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation-SDK-Beispiele](media-foundation-sdk-samples.md)
</dt> <dt>

[Medien senken](media-sinks.md)
</dt> </dl>

 

 



