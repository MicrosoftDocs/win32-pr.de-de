---
description: Synchronisieren von DVD-Befehlen
ms.assetid: 37e8f940-617d-43f6-92bd-aadccafe0059
title: Synchronisieren von DVD-Befehlen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4d677c38363a0ab80f90f58498eeef24bdc29eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106362710"
---
# <a name="synchronizing-dvd-commands"></a>Synchronisieren von DVD-Befehlen

DVD-Befehle sind nicht immer sofort fertiggestellt. Aus diesem Grund sind einige der Methoden in [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) asynchron. Dazu zählen Wiedergabe Methoden wie **playtitle** und Menü Navigationsmethoden, z. b. **showmenu** und **returnfromsubmenu**. Eine asynchrone Methode wird sofort zurückgegeben, ohne auf den Abschluss des Befehls zu warten. Nachdem die-Methode zurückgegeben wurde, können andere Ereignisse den Abschluss des Befehls verhindern, auch wenn die Methode erfolgreich ausgeführt wurde. DirectShow bietet verschiedene Optionen zum Synchronisieren von Befehlen, die von der Synchronisierung bis zur vollständigen Synchronisierung mithilfe von Filter Diagramm Ereignissen reichen.

Alle asynchronen Methoden verfügen über einen *dwFlags* -Parameter und einen *ppcmd* -Parameter. Der *dwFlags* -Parameter gibt das Synchronisierungs Verhalten an, und der *ppcmd* -Parameter gibt einen Zeiger auf ein optionales Synchronisierungs Objekt zurück. Je nachdem, welche Werte Sie für diese Parameter angeben, gibt es unterschiedliche Verhaltensweisen.

**Keine Synchronisierung**

Bei einer einfachen DVD-Wiedergabe Anwendung ist es möglicherweise einfach, Synchronisierungs Probleme zu ignorieren. Gelegentlich kann es vorkommen, dass ein Befehl fehlschlägt oder die Benutzeroberfläche bei der Aktualisierung geringfügig verzögert wird, diese Fehler jedoch in der Reihenfolge der Sekundenbruchteile liegen.

Um einen Befehl ohne Synchronisierung auszugeben, legen Sie das DVD- \_ cmd \_ -Flag " \_ None" im *dwFlags* -Parameter fest, und legen Sie den *ppcmd* -Parameter auf **null** fest:


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, NULL);
```



**Blockierung**

Wenn Sie das \_ schlüsselblockflag für die EC-DVD \_ \_ \_ im *dwFlags* -Parameter festlegen, wird die-Methode blockiert, bis der Befehl abgeschlossen ist:


```C++
hr = pDVDControl2->PlayTitle(uTitle, EC_DVD_CMD_FLAG_Block, NULL);
```



Dieses Flag wandelt eine asynchrone Methode in eine synchrone Methode um. Der Nachteil ist, dass die Benutzeroberfläche blockiert wird, wenn Sie die-Methode aus dem Anwendungs Thread aufzurufen.

**Synchronisierungs Objekt**

Alle asynchronen Methoden können ein Synchronisierungs Objekt zurückgeben, das Sie verwenden können, um auf das Starten oder Beenden des Befehls zu warten. Um dieses Objekt zu erhalten, übergeben Sie die Adresse eines [**idvdcmd**](/windows/desktop/api/Strmif/nn-strmif-idvdcmd) -Zeigers im *ppcmd* -Parameter:


```C++
IDvdCmd *pCmdObj = NULL;
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_None, &pCmdObj);
```



Wenn die Methode erfolgreich ausgeführt wird, gibt Sie ein neues **idvdcmd** -Objekt zurück. Die [**idvdcmd:: waitforstart**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforstart) -Methode blockiert, bis der Befehl beginnt, und die [**idvdcmd:: waitforend**](/windows/desktop/api/Strmif/nf-strmif-idvdcmd-waitforend) -Methode blockiert, bis der Befehl beendet wird. Der Rückgabewert gibt den Status des Befehls an.

Der folgende Code ist funktional äquivalent zum Festlegen des \_ \_ \_ zuvor gezeigten Flag für das "EC-DVD-cmd-Flag" \_ .


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



In diesem Fall wird die **playtitle** -Methode nicht blockiert, aber die Anwendung wird durch den Aufruf von **waitforend** blockiert.

**Befehls Status Ereignisse**

Wenn Sie \_ \_ \_ im *dwFlags* -Parameter das Flag sendevents für das DVD-cmd-Flag festlegen, sendet der DVD-Navigator ein [**EC-DVD- \_ \_ cmd- \_ Start**](ec-dvd-cmd-start.md) Ereignis, wenn der Befehl beginnt, und ein [**EC-DVD- \_ \_ cmd \_**](ec-dvd-cmd-end.md) -Ereignis, wenn der Befehl endet.

Der *lParam2* -Parameter des Ereignisses ist der HRESULT-Rückgabewert für den Befehl. Der *lParam1* -Parameter des Ereignisses bietet eine Möglichkeit, das Synchronisierungs Objekt für den Befehl zu erhalten. Wenn Sie *lParam1* an die [**IDvdInfo2:: getcmdfromevent**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcmdfromevent) -Methode übergeben, gibt die Methode einen Zeiger auf die **idvdcmd** -Schnittstelle des Synchronisierungs Objekts zurück. Sie können diese Schnittstelle verwenden, um auf den Abschluss des Befehls zu warten, wie zuvor beschrieben. Wenn Sie jedoch **null** für den *ppcmd* -Parameter in der ursprünglichen **IDvdControl2** -Methode übergeben haben, erstellt der DVD-Navigator kein Synchronisierungs Objekt, und **getcmdfromevent** gibt E \_ Fail zurück.

Der folgende Code zeigt, wie Sie Befehlsstatus Ereignisse ohne Synchronisierungs Objekt verwenden können.


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



Beachten Sie, dass Sie ohne Synchronisierungs Objekt nicht erkennen können, welcher Befehl dem Ereignis zugeordnet ist. Der folgende Code zeigt, wie Ereignisse mit dem Synchronisierungs Objekt verwendet werden. Die Idee besteht darin, die Synchronisierungs Objekte in einer Liste zu speichern und dann Objekt Zeiger zu vergleichen, wenn Sie das [**\_ \_ cmd- \_ Start**](ec-dvd-cmd-start.md) Ereignis oder das [**EC-DVD- \_ \_ cmd- \_ Endereignis**](ec-dvd-cmd-end.md) erhalten.


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

Während der Wiedergabe puffert der DVD-Navigator Videodaten. Die Menge der gepufferten Daten variiert. Wenn der DVD-Navigator zu einem neuen Video wechselt, gehen die Daten, die sich bereits in der Pipeline befinden, nicht verloren, sodass der Übergang nahtlos verläuft. Wenn der DVD-Navigator einen Befehl ausgibt, werden die in der Pipeline bereits vorhandenen Datenstandard mäßig nicht geleert. Dies führt möglicherweise zu einer gewissen Latenz, bevor Sie die Auswirkungen des Befehls erkennen können, je nachdem, wie viele Daten gepuffert werden. Um die Reaktionsfähigkeit zu erhöhen, können Sie erzwingen, dass der DVD-Navigator geleert wird, indem Sie das Flag "DVD \_ cmd \_ Flag Flush" festlegen \_ .


```C++
hr = pDVDControl2->PlayTitle(uTitle, DVD_CMD_FLAG_Flush, NULL);
```



Dieses Flag kann mit einem der zuvor beschriebenen Flags kombiniert werden, wobei ein bitweises OR verwendet wird. Ein Nebeneffekt des Leerung besteht darin, dass möglicherweise ein Video verloren geht. verwenden Sie daher dieses Flag nicht, wenn Sie sicherstellen müssen, dass keine Lücken im Video vorhanden sind.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DVD-Anwendungen](dvd-applications.md)
</dt> </dl>

 

 



