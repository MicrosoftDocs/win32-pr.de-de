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
ms.openlocfilehash: 36ff09a81cac98edc6f14ded98ba9852501bfdfef4c5e40affa908c0ff710e1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119807530"
---
# <a name="to-identify-inputs-by-number"></a>So identifizieren Sie Eingaben nach Zahl

Jedes Beispiel, das Sie an den Writer übergeben, muss einer Eingabenummer zugeordnet sein. Jede Eingabenummer entspricht einem oder mehreren Datenströmen im Profil, die der Writer zum Schreiben der Datei verwendet. In einem Profil werden Medienquellen durch einen Verbindungsnamen identifiziert. Der Writer ordnet jedem Verbindungsnamen eine Eingabenummer zu, wenn Sie das Profil für den Writer festlegen. Bevor Sie Beispiele an den Writer übergeben können, müssen Sie bestimmen, welche Daten die einzelnen Eingaben erwarten. Sie können nicht davon ausgehen, dass die Eingaben in derselben Reihenfolge wie die Streams in einem Profil vorliegen, auch wenn dies häufig der Fall ist. Daher besteht die einzige zuverlässige Möglichkeit zum Abgleichen von Eingaben mit Streams darin, den Verbindungsnamen der Eingabe mit dem Verbindungsnamen des Streams zu vergleichen.

Führen Sie die folgenden Schritte aus, um die Verbindungsnamen und die entsprechenden Eingabenummern für ein geladenes Profil zu identifizieren:

1.  Erstellen Sie ein Writer-Objekt, und legen Sie ein profil fest, das verwendet werden soll. Weitere Informationen zum Festlegen von Profilen im Writer finden Sie unter [So verwenden Sie Profile mit dem Writer](to-use-profiles-with-the-writer.md). Sie sollten die Verbindungsnamen kennen, die für die Streams im Profil verwendet werden. Sie können den Verbindungsnamen aus dem Profil abrufen, indem Sie das Streamkonfigurationsobjekt für jeden Stream abrufen und [**IWMStreamConfig::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig-getconnectionname)aufrufen. Weitere Informationen zu Profilen und Streamkonfigurationsobjekten finden Sie unter [Arbeiten mit Profilen.](working-with-profiles.md)
2.  Rufen Sie die Gesamtzahl der Eingaben ab, indem [**Sie IWMWriter::GetInputCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputcount)aufrufen.
3.  Durchlaufen Sie alle Eingaben, und führen Sie jeweils die folgenden Schritte aus.
    -   Rufen Sie die [**IWMInputMediaProps-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwminputmediaprops) für die Eingabe ab, indem [**Sie IWMWriter::GetInputProps**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-getinputprops)aufrufen.
    -   Rufen Sie den Verbindungsnamen ab, der der Eingabenummer entspricht, indem [**Sie IWMInputMediaProps::GetConnectionName**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwminputmediaprops-getconnectionname)aufrufen. Nachdem Sie über den Verbindungsnamen verfügen, kennen Sie die Streams, die den vom Writer zugewiesenen Eingabenummern zugeordnet sind.

Im folgenden Beispielcode wird der Verbindungsname für jede Eingabe angezeigt. Weitere Informationen zur Verwendung dieses Codes finden Sie unter [Verwenden der Codebeispiele.](using-the-code-examples.md)


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

[**IWMWriter-Schnittstelle**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriter)
</dt> <dt>

[**Schreiben von ASF-Dateien**](writing-asf-files.md)
</dt> </dl>

 

 




