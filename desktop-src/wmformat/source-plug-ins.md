---
title: Quell-Plug-Ins
description: Quell-Plug-Ins
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows Medienformat-SDK, Quell-Plug-Ins
- Advanced Systems Format (ASF), Quell-Plug-Ins
- ASF (Advanced Systems Format), Quell-Plug-Ins
- Quell-Plug-Ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f16d0edc82423a43e50591fa07e14623adc23b94234a28985afca8a496822a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845804"
---
# <a name="source-plug-ins"></a>Quell-Plug-Ins

Ein Quell-Plug-In ist eine Option, die Entwicklern zur Verfügung steht, die ihr eigenes Speichersystem für Windows Medien® implementieren möchten. Ein Quell-Plug-In ermöglicht dies durch die Implementierung einer COM-Schnittstelle namens **IStream,** bei der es sich um eine Standardschnittstelle zum Bereitstellen von Daten handelt.

Das Quell-Plug-In sollte als DLL geschrieben werden, und sein Vorhandensein wird dem SDK über einen Registrierungseintrag bekannt gemacht. Auf diese Weise kann eine beliebige Anzahl von Quell-Plug-Ins implementiert werden. Das Quell-Plug-In muss die [**WMCreateStreamForURL-Funktion**](wmcreatestreamforurl.md) exportieren.

Um ein Quell-Plug-In zu registrieren, sollte der folgende Registrierungseintrag hinzugefügt werden:

HKEY \_ LOCAL MACHINE Software Microsoft Windows Media \_ \\ \\ \\ \\ WMSDK-Quellen \\

Name = "beliebiger eindeutiger Name"

Wert = Pfadname der Quell-Plug-In-DLL

Nachdem die DLL registriert wurde, kann die Anwendung die **IWMReader::Open-Methode** (mit der entsprechenden URL als Parameter) verwenden, um auf Datenstromdaten zu zugreifen, die in Dateien oder benutzerdefinierten Datencontainern gespeichert werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**IWMReader::Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> <dt>

[**WMCreateStreamForURL**](wmcreatestreamforurl.md)
</dt> </dl>

 

 




