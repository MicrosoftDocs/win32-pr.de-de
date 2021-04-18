---
description: Dieses Programm überprüft das vorhanden sein und die Konfiguration der microsofttablet-PCs und der Berührungs Technologie-Kernkomponenten.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Beispiel für Tablet PC Platform Info
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d815f21233b1edcc90d456df68b3736c170a5fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352713"
---
# <a name="tablet-pc-platform-info-sample"></a><span data-ttu-id="f6577-103">Beispiel für Tablet PC Platform Info</span><span class="sxs-lookup"><span data-stu-id="f6577-103">Tablet PC Platform Info Sample</span></span>

<span data-ttu-id="f6577-104">Dieses Programm überprüft das vorhanden sein und die Konfiguration der microsofttablet-PCs und der Berührungs Technologie-Kernkomponenten.</span><span class="sxs-lookup"><span data-stu-id="f6577-104">This program checks the presence and configuration of the MicrosoftTablet PC and Touch Technology core components.</span></span> <span data-ttu-id="f6577-105">Es bestimmt, ob Tablet PC-Komponenten im Betriebssystem aktiviert sind, und listet Namen und Versionsinformationen für Kern Steuerelemente und die standardmäßige Handschrift-und Spracherkennung auf.</span><span class="sxs-lookup"><span data-stu-id="f6577-105">It determines whether Tablet PC components are enabled in the operating system, listing names and version information for core controls and the default handwriting and speech recognizer.</span></span>

<span data-ttu-id="f6577-106">Die Anwendung verwendet die GetSystemMetrics-Windows-API, indem \_ Sie SM TabletPC übergibt, um zu bestimmen, ob die Anwendung auf einem Tablet PC ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f6577-106">The application uses the GetSystemMetrics Windows API, passing in SM\_TABLETPC, to determine whether the application running on a Tablet PC.</span></span> <span data-ttu-id="f6577-107">SM \_ TabletPC ist in winuser. h definiert.</span><span class="sxs-lookup"><span data-stu-id="f6577-107">SM\_TABLETPC is defined in WinUser.h.</span></span>

<span data-ttu-id="f6577-108">Besonders interessant ist die Art und Weise, in der die Anwendung die Erkennungs Modul Auflistung verwendet, um Informationen über die Standard Erkennung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f6577-108">Of particular interest is the way the application uses the Recognizers collection to provide information about the default recognizer.</span></span> <span data-ttu-id="f6577-109">Bevor Sie versuchen, das Auflistungs-und Erkennungs Objekt der Erkennung zu verwenden, testet die Anwendung, dass Sie erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f6577-109">Before attempting to use the Recognizers collection and Recognizer object, the application tests for their successful creation.</span></span>

## <a name="components"></a><span data-ttu-id="f6577-110">Komponenten</span><span class="sxs-lookup"><span data-stu-id="f6577-110">Components</span></span>

<span data-ttu-id="f6577-111">Mithilfe des verteilbaren Mergemoduls können bestimmte Teile der Tablet PC Platform-API auf nicht-Tablet-Versionen von Vista und Windows XP Professional installiert werden.</span><span class="sxs-lookup"><span data-stu-id="f6577-111">Using the re-distributable merge module, certain parts of the Tablet PC Platform API may be installed on non-Tablet versions of Vista and Windows XP Professional .</span></span> <span data-ttu-id="f6577-112">Der GetSystemMetrics-Rückruf gibt nur an, dass die Windows XP Tablet PC Edition installiert ist.</span><span class="sxs-lookup"><span data-stu-id="f6577-112">The GetSystemMetrics call only indicates that Windows XP Tablet PC Edition is installed.</span></span> <span data-ttu-id="f6577-113">Eine Anwendung sollte immer ermitteln, ob eine bestimmte Komponente verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="f6577-113">An application should always determine if a given component is available.</span></span> <span data-ttu-id="f6577-114">Die richtige Möglichkeit, um zu bestimmen, ob eine Komponente der API installiert ist, besteht darin, eine Instanz eines Objekts oder eines Steuer Elements zu erstellen und zu überprüfen, ob es vorhanden ist, bevor Sie versuchen, es zu verwenden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="f6577-114">The proper way to determine if a component of the API is installed is to attempt to create an instance of an object or control and check that it exists before attempting to use it, as shown in the following example.</span></span>


```C++
IInkRecognizers* pIInkRecognizers = NULL;
HRESULT hr = CoCreateInstance(CLSID_InkRecognizers,
                              NULL, 
                              CLSCTX_INPROC_SERVER, 
                              IID_IInkRecognizers, 
                              (void **)&pIInkRecognizers);
if (SUCCEEDED(hr)) 
{
  // use the component
} else
{
  // component unavailable
}
```



<span data-ttu-id="f6577-115">Die Anwendung ermittelt die installierten Sprachkomponenten, indem Sie den entsprechenden Registrierungsschlüssel ansieht:</span><span class="sxs-lookup"><span data-stu-id="f6577-115">The application finds out about the installed speech components by looking in the appropriate registry key:</span></span>


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



<span data-ttu-id="f6577-116">Der Schlüssel wird mit regqueryvalueexw gelesen.</span><span class="sxs-lookup"><span data-stu-id="f6577-116">The key is read using RegQueryValueExW.</span></span>

<span data-ttu-id="f6577-117">Schließlich ermittelt das Beispiel, welche Steuerelemente installiert werden.</span><span class="sxs-lookup"><span data-stu-id="f6577-117">Finally, the sample finds out which controls are installed.</span></span>


```C++
LPCOLESTR gc_wszProgId[NUM_CONTROLS] = {L"InkEd.InkEdit", L"msinkaut.InkOverlay"};
// ...
for (int i = 0, j = 0; i < NUM_CONTROLS; i++)
{
    // Get the component info
    CLSID clsid;
    if (SUCCEEDED(CLSIDFromProgID(gc_wszProgId[i], &clsid)) && GetComponentInfo(clsid, info) == TRUE)
    {
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][0], info.wchName);
        SetDlgItemTextW(hwnd, gc_uiCtrlId[j][1], info.wchVersion);
        j++;
    }
}
```



 

 



