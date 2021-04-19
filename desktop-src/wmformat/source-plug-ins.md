---
title: Quell-Plug-ins
description: Quell-Plug-ins
ms.assetid: 9adc2d42-6273-4af0-b57f-2dde5738ed94
keywords:
- Windows Media-Format-SDK, Quell-Plug-ins
- Advanced Systems Format (ASF), Quell-Plug-ins
- ASF (Advanced Systems Format), Quell-Plug-ins
- Quell-Plug-ins
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4822b9110def4e1b758be40310f503fd56a251fd
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339870"
---
# <a name="source-plug-ins"></a>Quell-Plug-ins

Ein Quell-Plug-in ist eine Option, die Entwicklern zur Verfügung steht, die ihr eigenes Speichersystem für Windows Media®-Dateien implementieren möchten. Ein Quell-Plug-in ermöglicht dies durch die Implementierung einer COM-Schnittstelle namens **IStream**, bei der es sich um eine Standardschnittstelle zum Bereitstellen von Daten handelt.

Das Quell-Plug-in muss als DLL geschrieben werden, und seine Anwesenheit wird dem SDK über einen Registrierungs Eintrag bekannt gemacht. Auf diese Weise kann eine beliebige Anzahl von Quell-Plug-Ins implementiert werden. Das Quell-Plug-in muss die [**wmkreatestreamforurl**](wmcreatestreamforurl.md) -Funktion exportieren.

Zum Registrieren eines Quell-Plug-ins sollte der folgende Registrierungs Eintrag hinzugefügt werden:

HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Media \\ wmsdk- \\ Quellen

Name = "beliebiger eindeutiger Name"

Value = Pfadnamen der Quell-Plug-in-dll

Nachdem die dll registriert wurde, kann die Anwendung die **iwmreader:: Open** -Methode (mit der entsprechenden URL als Parameter) verwenden, um auf Streamdaten zuzugreifen, die in Dateien oder benutzerdefinierten Daten Containern gespeichert werden können.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmreader:: Open**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreader-open)
</dt> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> <dt>

[**Wmkreatestreamforurl**](wmcreatestreamforurl.md)
</dt> </dl>

 

 




