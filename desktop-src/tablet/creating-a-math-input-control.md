---
description: Erläutert, wie ein mathematisches Eingabesteuerelement erstellt wird.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Erstellen eines Steuerung für mathematische Eingaben
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ee8cca2a799bd44e79ef2f32691614bb3f22c933b40aa23dc4aa0cd6cfb6fb3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967719"
---
# <a name="creating-a-math-input-control"></a>Erstellen eines Steuerung für mathematische Eingaben

Zum Erstellen des mathematischen Eingabesteuerelements müssen Sie Folgendes beachten:

-   [Einschließen von Headern und Bibliotheken für die Steuerung für mathematische Eingaben](#include-headers-and-libraries-for-the-math-input-control)
-   [Deklarieren des Steuerelementzeigers und Aufrufen von CoInitialize für den Steuerelementzeiger](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [Anzeigen des Steuerelements](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>Einschließen von Headern und Bibliotheken für die Steuerung für mathematische Eingaben

Der folgende Code sollte oben im Code platziert werden, wo Sie das mathematische Eingabesteuerelement verwenden.


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



Dieser Code fügt Ihrer Anwendung Unterstützung für das mathematische Eingabesteuerelement hinzu.

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>Deklarieren des Steuerelementzeigers und Aufrufen von CoInitialize für den Steuerelementzeiger

Nachdem Sie die Header für das Steuerelement eingeschlossen haben, können Sie den Steuerelementzeiger deklarieren und CoInitialize dafür aufrufen, um ein Handle für die mathematische Eingabesteuerelementschnittstelle zu erstellen. Der folgende Code kann in einer Klasse oder als globale Variable in der Implementierung Ihrer Anwendung platziert werden:


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



Der folgende Code zeigt, wie Sie CoInitialize für den Steuerelementzeiger aufrufen können.


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



Nachdem Sie CoInitialize für den Steuerelementzeiger aufgerufen haben, verfügen Sie über einen Verweis auf das Steuerelement und können auf die Methoden des Steuerelements zugreifen. Sie können z. B. den erweiterten Satz von Steuerelementen aktivieren, wie im folgenden Beispiel gezeigt.


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>Anzeigen des Steuerelements

Das Steuerelement wird nicht automatisch angezeigt, nachdem Sie es erstellt haben. Rufen Sie zum Anzeigen des Steuerelements die [**Show-Methode**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) für den Steuerelementverweis auf, den Sie im vorherigen Schritt erstellt haben. Der folgende Code veranschaulicht, wie die [**Show-Methode**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) aufgerufen werden kann.


```
   hr = g_spMIC->Show();
   
```



Nachdem das Steuerelement angezeigt wird, sieht es in etwa wie in der folgenden Abbildung aus.

![Screenshot: Mathematisches Eingabesteuerelement](images/mic.png)

Beachten Sie, dass ich den erweiterten Satz von Schaltflächen aktiviert habe, sodass **Wiederholung** und **Rückgängig** verfügbar sind.

 

 
