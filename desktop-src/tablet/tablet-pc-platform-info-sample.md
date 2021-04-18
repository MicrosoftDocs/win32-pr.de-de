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
# <a name="tablet-pc-platform-info-sample"></a>Beispiel für Tablet PC Platform Info

Dieses Programm überprüft das vorhanden sein und die Konfiguration der microsofttablet-PCs und der Berührungs Technologie-Kernkomponenten. Es bestimmt, ob Tablet PC-Komponenten im Betriebssystem aktiviert sind, und listet Namen und Versionsinformationen für Kern Steuerelemente und die standardmäßige Handschrift-und Spracherkennung auf.

Die Anwendung verwendet die GetSystemMetrics-Windows-API, indem \_ Sie SM TabletPC übergibt, um zu bestimmen, ob die Anwendung auf einem Tablet PC ausgeführt wird. SM \_ TabletPC ist in winuser. h definiert.

Besonders interessant ist die Art und Weise, in der die Anwendung die Erkennungs Modul Auflistung verwendet, um Informationen über die Standard Erkennung bereitzustellen. Bevor Sie versuchen, das Auflistungs-und Erkennungs Objekt der Erkennung zu verwenden, testet die Anwendung, dass Sie erfolgreich erstellt wurde.

## <a name="components"></a>Komponenten

Mithilfe des verteilbaren Mergemoduls können bestimmte Teile der Tablet PC Platform-API auf nicht-Tablet-Versionen von Vista und Windows XP Professional installiert werden. Der GetSystemMetrics-Rückruf gibt nur an, dass die Windows XP Tablet PC Edition installiert ist. Eine Anwendung sollte immer ermitteln, ob eine bestimmte Komponente verfügbar ist. Die richtige Möglichkeit, um zu bestimmen, ob eine Komponente der API installiert ist, besteht darin, eine Instanz eines Objekts oder eines Steuer Elements zu erstellen und zu überprüfen, ob es vorhanden ist, bevor Sie versuchen, es zu verwenden, wie im folgenden Beispiel gezeigt.


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



Die Anwendung ermittelt die installierten Sprachkomponenten, indem Sie den entsprechenden Registrierungsschlüssel ansieht:


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



Der Schlüssel wird mit regqueryvalueexw gelesen.

Schließlich ermittelt das Beispiel, welche Steuerelemente installiert werden.


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



 

 



