---
description: In diesem Abschnitt werden die imm-Schnittstellen beschrieben.
ms.assetid: 25092F1D-0B54-4E5E-AC9E-F8F3A0181482
title: Schnittstellen für Eingabemethoden-Manager
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 64bd04c02425aef19ed329867a5b228bd4838af8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373072"
---
# <a name="input-method-manager-interfaces"></a>Schnittstellen für Eingabemethoden-Manager

In diesem Abschnitt werden die imm-Schnittstellen beschrieben.



| Schnittstelle                                                            | BESCHREIBUNG                                                                                                                                    |
|----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ifecommon**](/windows/desktop/api/Msime/nn-msime-ifecommon)                                       | Bietet IME-bezogene Dienste, die für verschiedene Sprachen üblich sind.                                                                         |
| [**Ifedictionary**](/windows/desktop/api/Msime/nn-msime-ifedictionary)                               | Ermöglicht Clients den Zugriff auf ein Microsoft IME-Benutzerwörterbuch.                                                                                      |
| [**Ifelanguage**](/windows/desktop/api/Msime/nn-msime-ifelanguage)                                   | Stellt sprach Verarbeitungsdienste mithilfe von Microsoft IME bereit.                                                                                 |
| [**Iimepad**](/windows/desktop/api/Imepad/nn-imepad-iimepad)                                           | Fügt Text aus imepadapplets in apps ein, die die [**iimepadapplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) -Schnittstelle implementieren.                                 |
| [**Iimepadapplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet)                               | Eingaben von Zeichen folgen in Apps über die [**iimepad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) -Schnittstelle.                                                                     |
| [**Iimepluginditdiktattionarylist**](/windows/desktop/api/Msimeapi/nn-msimeapi-iimeplugindictdictionarylist) | Bietet Zugriff auf die Liste der IME-Plug-in-Wörterbücher.                                                                                       |
| [**Iimespecifyapplets**](/windows/desktop/api/Imepad/nn-imepad-iimespecifyapplets)                     | Gibt Methoden an, die vom [**iimepad**](/windows/desktop/api/Imepad/nn-imepad-iimepad) -Schnittstellen Objekt zum Emulieren der [**iimepadapplet**](/windows/desktop/api/Imepad/nn-imepad-iimepadapplet) -Schnittstelle aufgerufen werden. |



 

 

 



