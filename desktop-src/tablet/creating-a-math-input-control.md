---
description: Erläutert, wie ein mathematisches Eingabe Steuerelement erstellt wird.
ms.assetid: 59976b01-9032-4226-a160-e9b2d4b8b23b
title: Erstellen eines mathematischen Eingabe Steuer Elements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5084f29943395bc6781fe20598f86bdc08c6c61
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104549931"
---
# <a name="creating-a-math-input-control"></a>Erstellen eines mathematischen Eingabe Steuer Elements

Um das mathematische Eingabe Steuerelement zu erstellen, müssen Sie folgende Schritte ausführen:

-   [Einschließen von Headern und Bibliotheken für das mathematische Eingabe Steuerelement](#include-headers-and-libraries-for-the-math-input-control)
-   [Deklarieren Sie den Steuerelement Zeiger, und rufen Sie CoInitialize im Steuerelement Zeiger auf](#declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer)
-   [Steuerelement anzeigen](#show-the-control)

## <a name="include-headers-and-libraries-for-the-math-input-control"></a>Einschließen von Headern und Bibliotheken für das mathematische Eingabe Steuerelement

Der folgende Code sollte am Anfang des Codes platziert werden, in dem Sie das mathematische Eingabe Steuerelement verwenden werden.


```
   // includes for implementation
   #include "micaut.h"
   #include "micaut_i.c"
   
```



Mit diesem Code wird der Anwendung Unterstützung für das mathematische Eingabe Steuerelement hinzugefügt.

## <a name="declare-the-control-pointer-and-call-coinitialize-on-the-control-pointer"></a>Deklarieren Sie den Steuerelement Zeiger, und rufen Sie CoInitialize im Steuerelement Zeiger auf

Nachdem Sie die Header für das-Steuerelement eingefügt haben, können Sie den Steuerelement Zeiger deklarieren und CoInitialize darauf abrufen, um ein Handle für die mathematische Eingabe Steuerungs Schnittstelle zu erstellen. Der folgende Code kann in einer Klasse oder als globale Variable in der Implementierung der Anwendung platziert werden:


```
   CComPtr<IMathInputControl> g_spMIC; // Math Input Control
   
```



Der folgende Code zeigt, wie Sie CoInitialize auf dem Steuerelement Zeiger abrufen können.


```
   HRESULT hr = CoInitialize(NULL);
   hr = g_spMIC.CoCreateInstance(CLSID_MathInputControl);
   
```



Nach dem Aufrufen von CoInitialize für den Steuerelement Zeiger verfügen Sie über einen Verweis auf das Steuerelement und können auf die Methoden des Steuer Elements zugreifen. Beispielsweise können Sie den erweiterten Satz von Steuerelementen aktivieren, wie im folgenden Beispiel gezeigt.


```
   hr = g_spMIC->EnableExtendedButtons(VARIANT_TRUE);
   
```



## <a name="show-the-control"></a>Steuerelement anzeigen

Das Steuerelement wird nach der Erstellung nicht automatisch angezeigt. Um das Steuerelement anzuzeigen, nennen Sie die [**Show**](/windows/desktop/api/micaut/nf-micaut-imathinputcontrol-show) -Methode für den Steuerelement Verweis, den Sie im vorherigen Schritt erstellt haben. Der folgende Code veranschaulicht, wie die [**Show**](/windows/win32/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_autoshow) -Methode aufgerufen werden kann.


```
   hr = g_spMIC->Show();
   
```



Nachdem das Steuerelement angezeigt wird, sieht es in etwa wie in der folgenden Abbildung aus.

![Screenshot mit mathematischer Eingabesteuerung](images/mic.png)

Beachten Sie, dass der erweiterte Satz von Schaltflächen aktiviert ist, sodass wieder **holen** und **Rückgängig** gemacht werden können.

 

 
