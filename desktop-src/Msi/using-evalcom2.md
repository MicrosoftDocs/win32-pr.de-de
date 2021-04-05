---
description: Evalcom2.dll können zur Implementierung von Validierungs Vorgängen für Installationspakete und Mergemodule mithilfe interner Konsistenz Auswertungen-ICES verwendet werden.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Verwenden von Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c49a165115b505d5c78ebe5b5e714b8a3c359d72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751696"
---
# <a name="using-evalcom2"></a>Verwenden von Evalcom2

Evalcom2.dll können zur Implementierung von Validierungs Vorgängen für Installationspakete und Mergemodule mithilfe [interner Konsistenz Auswertungen-ICES](internal-consistency-evaluators-ices.md)verwendet werden. Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme.

Das Hauptobjekt implementiert auch [Evalcom2-Schnittstellen](evalcom2-interfaces.md) für C/C++-Programme. Die zum Abrufen der Schnittstelle von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) erforderliche CLSID ist {6e5e1910-8053-4660-B795-6b612e29bc58}. Die refid ist {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.

Mit dem folgenden Verfahren können Sie Validierungs Vorgänge implementieren.

**So implementieren Sie Validierungs Vorgänge**

1.  Initialisieren Sie com auf dem aufrufenden Thread mithilfe von [**CoInitialize**](/windows/win32/api/objbase/nf-objbase-coinitialize).
2.  Rufen Sie mithilfe von [**cokreateinstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance)den Zeiger auf die [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) -Schnittstelle ab.
3.  Öffnen Sie das Installationspaket oder Mergemodul mithilfe der [**OpenDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase) -Methode.
4.  Öffnen Sie die Auswertungs Datei mithilfe der [**opencub**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub) -Methode.
5.  Legen Sie die Anzeige Rückruffunktion mithilfe der [**setdisplay**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) -Methode fest.
6.  Legen Sie die Status Rückruffunktion mithilfe der [**SetStatus**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) -Methode fest.
7.  Führen Sie die Validierung mithilfe der [**Validate**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) -Methode aus.
8.  Schließen Sie die CUB-Datei mithilfe der [**closecub**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub) -Methode.
9.  Schließen Sie die Datenbank mit der [**CloseDatabase**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase) -Methode.
10. Geben Sie die [**IValidate**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) -Schnittstelle frei.
11. Initialisieren Sie com mithilfe von " [**zählinitialize**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)".

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Evalcom2-Schnittstellen](evalcom2-interfaces.md)
</dt> <dt>

[Validierungs Automatisierung](validation-automation.md)
</dt> <dt>

[Validierungs Rückruf Funktionen](validation-callback-functions.md)
</dt> </dl>

 

 
