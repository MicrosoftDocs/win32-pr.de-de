---
description: In diesem Abschnitt werden die IMM-Schnittstellen beschrieben.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Schnittstellen des Eingabemethode-Managers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3e7267f5f38bb160a7f71b4f0379a2b03a3263b85a64dc8e666226dd3150911
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117809999"
---
# <a name="input-method-manager-interfaces"></a>Schnittstellen des Eingabemethode-Managers

In diesem Abschnitt werden die IMM-Schnittstellen beschrieben.



| Schnittstelle                                                            | BESCHREIBUNG                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IFECommon**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | Stellt IME-bezogene Dienste zur Verfügung, die für verschiedene Sprachen üblich sind.                                                                         |
| [**IFEDictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | Ermöglicht Clients den Zugriff auf ein Microsoft IME-Benutzerwörterbuch.                                                                                      |
| [**IFELanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | Stellt Sprachverarbeitungsdienste mithilfe des Microsoft IME zur Verfügung.                                                                                 |
| [**IImePad**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | Fügt Text aus IMEPadApplets in Apps ein, die die [**IImePadApplet-Schnittstelle**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) implementieren.                                 |
| [**IImePadApplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | Gibt Zeichenfolgen über die [**IImePad-Schnittstelle in Apps**](/windows/desktop/api/Imepad/nn-imepad-iimepad) ein.                                                                     |
| [**IImePlugInDictDictionaryList**](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | Ermöglicht den Zugriff auf die Liste der IME-Plug-In-Wörterbücher.                                                                                       |
| [**IImeSpecifyApplets**](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | Gibt Methoden an, die vom [**IImePad-Schnittstellenobjekt**](/windows/desktop/api/Imepad/nn-imepad-iimepad) aufgerufen werden, um die [**IImePadApplet-Schnittstelle zu emulieren.**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) |



 

 

 



