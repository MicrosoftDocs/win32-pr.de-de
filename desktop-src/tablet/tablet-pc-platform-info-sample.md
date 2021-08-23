---
description: Dieses Programm überprüft das Vorhandensein und die Konfiguration der Kernkomponenten MicrosoftTablet PC und Touch Technology.
ms.assetid: 0b379dc9-a86f-40c0-9403-d9c9091ca8c3
title: Tablet PC Platform Info Sample
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1731fc30e0405b2702bb45d0a9d0556b861ad09994ac683d739da33afe018088
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119819981"
---
# <a name="tablet-pc-platform-info-sample"></a>Tablet PC Platform Info Sample

Dieses Programm überprüft das Vorhandensein und die Konfiguration der Kernkomponenten MicrosoftTablet PC und Touch Technology. Sie bestimmt, ob Tablet PC-Komponenten im Betriebssystem aktiviert sind, und listet Namen und Versionsinformationen für Kernsteuerelemente sowie die Standardhandschreibung und Spracherkennung auf.

Die Anwendung verwendet die GetSystemMetrics Windows-API und übergibt SM \_ TABLETPC, um zu bestimmen, ob die Anwendung auf einem Tablet-PC ausgeführt wird. SM \_ TABLETPC ist in WinUser.h definiert.

Von besonderem Interesse ist die Art und Weise, wie die Anwendung die Recognizers-Auflistung verwendet, um Informationen über die Standarderkennung bereitzustellen. Bevor versucht wird, die Recognizers-Auflistung und das Recognizer-Objekt zu verwenden, testet die Anwendung ihre erfolgreiche Erstellung.

## <a name="components"></a>Komponenten

Mithilfe des wiederverteilbaren Mergemoduls können bestimmte Teile der Tablet PC Platform-API auf Nicht-Tablet-Versionen von Vista und Windows XP Professional installiert werden. Der GetSystemMetrics-Aufruf gibt nur an, dass Windows XP Tablet PC Edition installiert ist. Eine Anwendung sollte immer bestimmen, ob eine bestimmte Komponente verfügbar ist. Die richtige Methode, um zu bestimmen, ob eine Komponente der API installiert ist, besteht darin, eine Instanz eines Objekts oder Steuerelements zu erstellen und zu überprüfen, ob es vorhanden ist, bevor Sie versuchen, es zu verwenden, wie im folgenden Beispiel gezeigt.


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



Die Anwendung ermittelt die installierten Speech-Komponenten, indem sie den entsprechenden Registrierungsschlüssel sucht:


```C++
const WCHAR* gc_wszSpeechKey = L"Software\\Microsoft\\Speech\\Recognizers";
//...
if (RegOpenKeyExW(HKEY_LOCAL_MACHINE, gc_wszSpeechKey, 0, KEY_READ, 
                  &hkeySpeech) == ERROR_SUCCESS) 
```



Der Schlüssel wird mithilfe von RegQueryValueExW gelesen.

Schließlich wird im Beispiel ermittelt, welche Steuerelemente installiert sind.


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



 

 



