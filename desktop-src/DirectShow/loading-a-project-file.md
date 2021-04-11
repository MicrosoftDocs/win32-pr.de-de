---
description: Laden einer Projektdatei
ms.assetid: f8d142bd-e51d-4714-893b-8e3d02506891
title: Laden einer Projektdatei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f9a710795a29481740bf85390cc7122cc801a22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104213901"
---
# <a name="loading-a-project-file"></a>Laden einer Projektdatei

\[Diese API wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.\]

Zum Laden einer Projektdatei benötigen Sie zwei Komponenten: den XML-Parser und eine leere Zeitachse. Der XML-Parser liest eine XML-Projektdatei und erstellt jedes Objekt, das in der Datei definiert ist. Anschließend werden die Objekte in die Zeitachse eingefügt, und es werden alle Zeitachsen Attribute festgelegt, z. b. die Standard Frame Rate Im folgenden Codebeispiel wird eine Datei geladen.


```C++
HRESULT         hr;
IAMTimeline     *pTL = NULL;
IXml2Dex        *pXML = NULL; 
hr = CoCreateInstance(CLSID_AMTimeline, NULL, CLSCTX_INPROC_SERVER, 
            IID_IAMTimeline, (void**)&pTL);
hr = CoCreateInstance(CLSID_Xml2Dex, NULL, CLSCTX_INPROC_SERVER, 
            IID_IXml2Dex, (void**)&pXML);
BSTR bstrFile = SysAllocStringLen(OLESTR("C:\\example.xtl"), 15);
hr = pXML->ReadXMLFile(pTL, bstrFile); 
SysFreeString(bstrFile);
pXML->Release();
```



Der Parser macht die [**IXml2Dex**](ixml2dex.md) -Schnittstelle verfügbar, die Methoden zum Laden und Speichern von Projektdateien enthält. Die Zeitachse macht die [**iamtimeline**](iamtimeline.md) -Schnittstelle verfügbar, die Methoden zum Bearbeiten der Zeitachse und Erstellen neuer Zeitachsen Objekte enthält. Rufen Sie die **cokreateinstance** -Funktion auf, um jede Komponente zu erstellen, wie hier gezeigt. Beachten Sie, dass Sie durch das Erstellen einer neuen-Instanz den Verweis Zähler für die-Schnittstelle inkrementieren. Um Speicher Verluste zu vermeiden, geben Sie immer eine Schnittstelle frei, wenn Sie mit der Datei umgehen. In diesem Beispiel ist der Zeiger auf **IXml2Dex** nicht mehr erforderlich, sodass Sie die-Schnittstelle freigeben können. Der Zeiger auf **iamtimeline** ist nach wie vor für die Vorschau der Zeitachse erforderlich.

Die [**IXml2Dex:: infoxmlfile**](ixml2dex-readxmlfile.md) -Methode liest die angegebene Datei und füllt die Zeitachse mit den in der Datei definierten Objekten auf. Der Dateiname wird mit einem **BSTR** -Wert angegeben. Um das Beispiel zu verkürzen, wird der Dateiname im Beispiel als Literalzeichenfolge angegeben. Normalerweise erhalten Sie diese aus einem geöffneten Datei Dialogfeld oder etwas ähnliches.

Wenn die Read **XML** -Methode erfolgreich ist, wird ein Erfolgs Code zurückgegeben. Andernfalls wird ein Fehlercode zurückgegeben, z \_ . b. VFW E \_ ungültiges \_ Datei \_ Format. Überprüfen Sie immer den Rückgabewert, um Fehlerbedingungen ordnungsgemäß zu behandeln. Aus Gründen der Übersichtlichkeit wird im Beispielcode nicht auf Fehler überprüft.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Laden und Anzeigen der Vorschau eines Projekts](loading-and-previewing-a-project.md)
</dt> </dl>

 

 



