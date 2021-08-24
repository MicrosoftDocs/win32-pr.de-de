---
description: Evalcom2.dll kann verwendet werden, um Validierungsvorgänge für Installationspakete und Mergemodule mit internen Konsistenzauswertungen – ICEs zu implementieren.
ms.assetid: df38e75e-554c-4a6d-b9ad-8eee5123a16f
title: Verwenden von Evalcom2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f89ba0215e697cb03111daa80510e6ba6c677c2e74f31e74b5640340d2d0d9a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119527122"
---
# <a name="using-evalcom2"></a>Verwenden von Evalcom2

Evalcom2.dll kann verwendet werden, um Validierungsvorgänge für Installationspakete und Mergemodule mithilfe der [internen Konsistenzauswertung – ICEs – zu implementieren.](internal-consistency-evaluators-ices.md) Das Hauptobjekt implementiert Schnittstellen für C/C++-Programme.

Das Hauptobjekt implementiert auch [Evalcom2-Schnittstellen](evalcom2-interfaces.md) für C/C++-Programme. Die CLSID, die zum Abrufen der Schnittstelle von [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance) erforderlich ist, ist {6E5E1910-8053-4660-B795-6B612E29BC58}. Die REFIID ist {E482E5C6-E31E-4143-A2E6-DBC3D8E4B8D3}.

Sie können das folgende Verfahren verwenden, um Validierungsvorgänge zu implementieren.

**So implementieren Sie Validierungsvorgänge**

1.  Initialisieren Sie COM im aufrufenden Thread [**mithilfe von CoInitialize.**](/windows/win32/api/objbase/nf-objbase-coinitialize)
2.  Abrufen des Zeigers auf die [**IValidate-Schnittstelle**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) [**mithilfe von CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).
3.  Öffnen Sie das Installationspaket oder Mergemodul mithilfe der [**OpenDatabase-Methode.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opendatabase)
4.  Öffnen Sie die Auswertungsdatei mithilfe der [**OpenCUB-Methode.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-opencub)
5.  Legen Sie die Anzeigerückruffunktion mithilfe der [**SetDisplay-Methode**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setdisplay) fest.
6.  Legen Sie die Statusrückruffunktion mithilfe der [**SetStatus-Methode**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-setstatus) fest.
7.  Führen Sie die Überprüfung mithilfe der [**Validate-Methode**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-validate) aus.
8.  Schließen Sie die CUB-Datei mithilfe der [**CloseCUB-Methode.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closecub)
9.  Schließen Sie die Datenbank mithilfe der [**CloseDatabase-Methode.**](/windows/desktop/api/evalcom2/nf-evalcom2-ivalidate-closedatabase)
10. Geben Sie die [**IValidate-Schnittstelle**](/windows/desktop/api/evalcom2/nn-evalcom2-ivalidate) frei.
11. Initialisieren Sie COM [**mithilfe von CoUninitialize.**](/windows/win32/api/combaseapi/nf-combaseapi-couninitialize)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Evalcom2-Schnittstellen](evalcom2-interfaces.md)
</dt> <dt>

[Validierungsautomatisierung](validation-automation.md)
</dt> <dt>

[Validierungsrückruffunktionen](validation-callback-functions.md)
</dt> </dl>

 

 
