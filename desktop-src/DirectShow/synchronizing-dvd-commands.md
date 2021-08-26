---
description: Synchronisieren von DVD-Befehlen
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Synchronisieren von DVD-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38696425892618f1b66544e69a4a567d0f539234d991cb96792eda4f6f1509d3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119964810"
---
# <a name="synchronizing-dvd-commands"></a>Synchronisieren von DVD-Befehlen

DVD-Befehle werden nicht immer sofort abgeschlossen. Aus diesem Grund sind einige der Methoden in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) asynchron. Dazu gehören Wiedergabemethoden wie **PlayTitle** und Menünavigationsmethoden wie **ShowMenu** und **ReturnFromSubmenu.** Eine asynchrone Methode gibt sofort zurück, ohne auf den Abschluss des Befehls zu warten. Nachdem die Methode zurückgegeben wurde, können andere Ereignisse den Abschluss des Befehls verhindern, selbst wenn die Methode erfolgreich war. DirectShow bietet mehrere Optionen zum Synchronisieren von Befehlen, die von keiner Synchronisierung bis hin zur vollständigen Synchronisierung mithilfe von Filterdiagrammereignissen reichen.

Alle asynchronen Methoden verfügen über einen *dwFlags-Parameter* und einen *ppCmd-Parameter.* Der *dwFlags-Parameter* gibt das Synchronisierungsverhalten an, und der *ppCmd-Parameter* gibt einen Zeiger auf ein optionales Synchronisierungsobjekt zurück. Je nachdem, welche Werte Sie für diese Parameter angeben, ergeben sich unterschiedliche Verhaltensweisen.

**Keine Synchronisierung**

Für eine einfache DVD-Wiedergabeanwendung ist es möglicherweise die beste Option, Synchronisierungsprobleme einfach zu ignorieren. Gelegentlich kann ein Befehl fehlschlagen, oder die Benutzeroberfläche kann bei der Aktualisierung geringfügig verzögert werden, aber diese Fehler liegen in der Reihenfolge von Sekundenbruchteilen.

Wenn Sie einen Befehl ohne Synchronisierung ausführen möchten, legen Sie das Flag DVD CMD FLAG None im dwFlags-Parameter und den \_ \_ \_ *ppCmd-Parameter* auf **NULL fest:** 


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



**Blockierung**

Wenn Sie das EC \_ DVD \_ CMD \_ FLAG \_ Block-Flag im *dwFlags-Parameter* festlegen, wird die Methode blockiert, bis der Befehl abgeschlossen ist:


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



Dieses Flag macht eine asynchrone Methode in eine synchrone Methode. Der Nachteil ist, dass ihre Benutzeroberfläche blockiert wird, wenn Sie die -Methode aus dem Anwendungsthread aufrufen.

**Synchronization-Objekt**

Alle asynchronen Methoden können ein Synchronisierungsobjekt zurückgeben, mit dem Sie warten können, bis der Befehl gestartet oder beendet wird. Um dieses Objekt zu erhalten, übergeben Sie die Adresse eines [**IDvdCmd-Zeigers**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) im *ppCmd-Parameter:*


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



Wenn die Methode erfolgreich ist, wird ein neues **IDvdCmd-Objekt** zurückgegeben. Die [**IDvdCmd::WaitForStart-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) wird blockiert, bis der Befehl beginnt, und die [**IDvdCmd::WaitForEnd-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) wird blockiert, bis der Befehl beendet wird. Der Rückgabewert gibt den Status des Befehls an.

Der folgende Code entspricht funktional dem Zuvor gezeigten EC \_ DVD \_ CMD \_ FLAG \_ Block-Flag.


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
if (SUCCEEDED(hr))
{
    // Use pCmdObj to wait for the command to complete.
    hr = pCmdObj->WaitToEnd();
    pCmdObj->Release();
}
```



In diesem Fall wird die **PlayTitle-Methode** nicht blockiert, aber die Anwendung blockiert durch Aufrufen **von WaitForEnd**.

**Befehlsstatusereignisse**

Wenn Sie das FLAG \_ SENDEvents des DVD-CMD-FLAGs im \_ \_ *dwFlags-Parameter* festlegen, sendet der DVD-Navigator ein [**EC DVD \_ \_ CMD \_ START-Ereignis,**](ec-dvd-cmd-start.md) wenn der Befehl beginnt, und ein EC DVD [**\_ \_ CMD \_ END-Ereignis,**](ec-dvd-cmd-end.md) wenn der Befehl beendet wird.

Der *lParam2-Parameter des* Ereignisses ist der HRESULT-Rückgabewert für den Befehl. Der *lParam1-Parameter* des Ereignisses bietet eine Möglichkeit, das Synchronisierungsobjekt für den Befehl zu erhalten. Wenn Sie *lParam1* an die [**IDvdInfo2::GetCmdFromEvent-Methode**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) übergeben, gibt die Methode einen Zeiger auf die **IDvdCmd-Schnittstelle** des Synchronisierungsobjekts zurück. Sie können diese Schnittstelle verwenden, um auf den Abschluss des Befehls zu warten, wie zuvor beschrieben. Wenn Sie jedoch  NULL für den *ppCmd-Parameter* in der ursprünglichen **IDvdControl2-Methode** übergeben haben, erstellt der DVD-Navigator kein Synchronisierungsobjekt, und **GetCmdFromEvent** gibt E \_ FAIL zurück.

Der folgende Code zeigt, wie Befehlsstatusereignisse ohne Synchronisierungsobjekt verwendet werden.


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, NULL);

// In your event handling code:
switch (lEvent)
{
   case EC_DVD_CMD_END:
       HRESULT hr2 = (HRESULT)lParam2;
       /* ... */ 
       break;
}
```



Beachten Sie, dass Sie ohne ein Synchronisierungsobjekt nicht erkennen können, welcher Befehl dem Ereignis zugeordnet ist. Der folgende Code zeigt, wie Ereignisse mit dem Synchronisierungsobjekt verwendet werden. Die Idee ist, die Synchronisierungsobjekte in einer Liste zu speichern und dann Objektzeige zu vergleichen, wenn Sie das [**EC \_ DVD \_ CMD \_ START-**](ec-dvd-cmd-start.md) oder [**EC DVD \_ \_ CMD \_ END-Ereignis**](ec-dvd-cmd-end.md) erhalten.


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_SendEvents, &pCmdObj);
if (SUCCEEDED(hr)) 
{
    // Store pCmdObj in a list of pending commands.
}

// In your event handling code:
switch (lEvent)
{
case EC_DVD_CMD_END:
   {
       IDvdCmd *pObj = NULL;
       hr = pDvdInfo2->GetCmdFromEvent(lParam, &pObj);
       if (SUCCEEDED(hr)) 
       {
           // Find this object in your list by comparing IUnknown
           // pointers. Assume the following function is defined in 
           // your application:
           IDvdCmd *pPendingObj = GetPendingCommandFromList(pObj); 
           if (pPendingObj)
           {
               // Update UI accordingly (not shown). 
               pPendingObj->Release();
           }
           pObj->Release();
       }
    }
    break;
} 
```



**Leeren der Puffer des DVD-Navigators**

Während der Wiedergabe puffert der DVD-Navigator Videodaten. Die Menge der gepufferten Daten variiert. Wenn der DVD-Navigator zu einem neuen Video wechselt, gehen daten, die sich bereits in der Pipeline befindet, nicht verloren, sodass der Übergang nahtlos ist. Wenn der DVD-Navigator einen Befehl aus gibt, werden standardmäßig keine Daten geleert, die bereits in der Pipeline enthalten sind. Daher kann es eine gewisse Latenz geben, bevor Sie die Auswirkungen des Befehls sehen können, je nachdem, wie viele Daten gepuffert werden. Um die Reaktionsfähigkeit zu erhöhen, können Sie erzwingen, dass der DVD-Navigator geleert wird, indem Sie das Flag DVD \_ CMD \_ FLAG Flush \_ festlegen.


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



Dieses Flag kann mit jedem der zuvor beschriebenen Flags kombiniert werden, indem ein bitweises OR verwendet wird. Ein Nebeneffekt der Leerung ist, dass ein Teil des Videos verloren gehen kann. Verwenden Sie daher dieses Flag nicht, wenn Sie garantieren müssen, dass es keine Lücken im Video gibt.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



