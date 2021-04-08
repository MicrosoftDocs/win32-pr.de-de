---
title: So identifizieren Sie Eingaben nach Zahl
description: So identifizieren Sie Eingaben nach Zahl
ms.assetid: f468f74d-7eed-4819-957d-241903f44d2d
keywords:
- Advanced Systems Format (ASF), Identifizieren von Eingaben nach Zahl
- ASF (Advanced Systems Format), Identifizieren von Eingaben nach Zahl
- Profile, Identifizieren von Eingaben nach Zahl
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0629776eaaff4252a690c0e31cd6002f5de42b31
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104038545"
---
# <a name="to-identify-inputs-by-number"></a>So identifizieren Sie Eingaben nach Zahl

Jedes Beispiel, das Sie an den Writer übergeben, muss einer Eingabe Nummer zugeordnet werden. Jede Eingabe Nummer entspricht einem oder mehreren Datenströmen in dem Profil, das der Writer zum Schreiben der Datei verwendet. In einem Profil werden Medienquellen anhand eines Verbindungs Namens identifiziert. Der Writer ordnet dem einzelnen Verbindungs Namen eine Eingabe Nummer zu, wenn Sie das Profil für den Writer festlegen. Bevor Sie Beispiele an den Writer übergeben können, müssen Sie bestimmen, welche Daten von den einzelnen Eingaben erwartet werden. Sie können nicht davon ausgehen, dass die Eingaben in derselben Reihenfolge wie die Datenströme in einem Profil vorliegen, auch wenn dies häufig der Fall ist. Daher ist die einzige zuverlässige Möglichkeit, Eingaben mit Streams abzugleichen, der Verbindungs Name der Eingabe mit dem Verbindungs Namen des Streams zu vergleichen.

Führen Sie die folgenden Schritte aus, um die Verbindungs Namen und die zugehörigen Eingabe Nummern für ein geladenes Profil zu identifizieren:

1.  Erstellen Sie ein Writer-Objekt, und legen Sie ein Profil zur Verwendung fest. Weitere Informationen zum Festlegen von Profilen im Writer finden [Sie unter So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md). Sie sollten die Verbindungs Namen kennen, die für die Datenströme im Profil verwendet werden. Sie können den Verbindungs Namen innerhalb des Profils abrufen, indem Sie das Datenstrom-Konfigurationsobjekt für jeden Stream abrufen und [**iwmstreamconfig:: getConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname)aufrufen. Weitere Informationen zu Profilen und Stream-Konfigurationsobjekten finden Sie unter [Arbeiten mit Profilen](working-with-profiles.md).
2.  Rufen Sie die Gesamtzahl der Eingaben durch Aufrufen von [**iwmwriter:: getinputcount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount)ab.
3.  Durchlaufen Sie alle Eingaben, und führen Sie jeweils die folgenden Schritte aus.
    -   Rufen Sie die [**iwminputmediarequicenschnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) für die Eingabe ab, indem Sie [**iwmwriter:: GetInput-**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)Eigenschaften aufrufen.
    -   Rufen Sie den Verbindungs Namen ab, der der Eingabe Nummer entspricht, indem Sie [**iwminputmedia-Eigenschaften:: getConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname)aufrufen. Nachdem Sie den Verbindungs Namen eingegeben haben, kennen Sie die Streams, die mit den vom Writer zugewiesenen Eingabe Nummern verknüpft sind.

Der folgende Beispielcode zeigt den Verbindungs Namen für jede Eingabe an. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele](using-the-code-examples.md).


```C++
HRESULT GetNamesForInputs(IWMWriter* pWriter)
{
    DWORD    cInputs  = 0;
    HRESULT  hr       = S_OK;
    WCHAR*   pwszName = NULL;
    WORD     cchName  = 0;

    IWMInputMediaProps* pProps = NULL;

    // Get the total number of inputs for the file.
    hr = pWriter->GetInputCount(&cInputs);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all supported inputs.
    for (DWORD inputIndex = 0; inputIndex < cInputs; inputIndex++)
    {
        // Get the input properties for the input.
        hr = pWriter->GetInputProps(inputIndex, &pProps);  
        GOTO_EXIT_IF_FAILED(hr);

        // Get the size of the connection name.
        hr = pProps->GetConnectionName(0, &cchName);
        GOTO_EXIT_IF_FAILED(hr);

        if (cchName > 0)
        {
            // Allocate memory for the connection name.
            pwszName = new WCHAR[cchName];
            if (wszName == NULL)
            {
                hr = E_OUTOFMEMORY;
                goto Exit;
            }

            // Get the connection name.
            hr = pProps->GetConnectionName(pwszName, &cchName);
            GOTO_EXIT_IF_FAILED(hr);
            
            // Display the name.
            printf("Input # %d = %S\n", pwszName);
        } // end if

        // Clean up for next iteration.
        SAFE_ARRAY_DELETE(pwszName);
        SAFE_RELEASE(pProps);
    } // end for inputIndex

Exit:
    SAFE_ARRAY_DELETE(pwszName);
    SAFE_RELEASE(pProps);
    return hr;
}

```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Iwmwriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




