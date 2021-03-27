---
description: Ein Gerät kann potenziell viele Ereignisse generieren, und jedes Ereignis hat die Möglichkeit, von einem von mehreren unterschiedlichen Handlern verarbeitet zu werden.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Registrieren eines Ereignis Handlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a3d786111a80cba455dd3480bdc970bc27009d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104979521"
---
# <a name="how-to-register-an-event-handler"></a>Registrieren eines Ereignis Handlers

Ein Gerät kann potenziell viele Ereignisse generieren, und jedes Ereignis hat die Möglichkeit, von einem von mehreren unterschiedlichen Handlern verarbeitet zu werden. In Windows XP sind die folgenden Ereignisse definiert:

-   Devicearrival
-   Deviceremoval
-   Mediaarrival
-   Mediaremuval

## <a name="instructions"></a>Instructions


Ereignishandler werden unter dem Schlüssel **Eventhandlers** definiert. Bei den Werten eines ereignishandlerschlüssels handelt es sich um die Namen der einzelnen Handler, aus denen der Benutzer auswählen muss, wenn das Ereignis erkannt wird. Diesen Einträgen ist kein Datenwert zugeordnet. Im folgenden finden Sie eine Beispiel Definition für einen benutzerdefinierten Ereignishandler mit dem Namen **mynewremovaleventhandler, der diese handlermöglichkeiten** für den Benutzer darstellt:

-   Ein Handler, der verwendet wird, wenn das Ereignis auf einem Gerät erkannt wird, das vom Unternehmen mit dem Namen "c-so, Inc."
-   Ein Handler, der verwendet wird, wenn das Ereignis auf einem Gerät erkannt wird, das vom Unternehmen mit dem Namen Fabrikam, Inc.
-   Ein Handler, der in allen anderen Fällen verwendet werden soll.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     EventHandlers
                        MyNewRemovalEventHandler
                           CompanyContosoHandler [REG_SZ]
                           CompanyFabrikamHandler [REG_SZ]
                           MyRemovalHandler [REG_SZ]
```

Nachdem ein Ereignishandler definiert wurde, muss er mit einem Geräte Handler für eine der Ereignis Möglichkeiten registriert werden: devicearrival, deviceremoval, mediaarrival oder mediaremoval. Mynewremovaleventhandler, der zuvor definiert wurde, wird für deviceremoval unter einem benutzerdefinierten Geräte Handler mit dem Namen mydevicehandler verwendet und für diesen Zweck im folgenden Beispiel definiert. Auch hier hat der Registrierungs Wert keine Daten Komponente.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  AutoplayHandlers
                     DeviceHandlers
                        EventHandlers
                           DeviceRemoval
                              MyNewRemovalEventHandler
```

In Windows XP wird der folgende Satz von EventHandler definiert. 

| Eventhandlers-Schlüssel        | Medien-oder Dateityp                             |
|--------------------------|------------------------------------------------|
| HandleCDBurningOnArrival | Leere CD-R/CD-RW                               |
| ShowPicturesOnArrival    | Bilddateien                                  |
| PlayMusicFilesOnArrival  | Musikdateien                                    |
| PlayVideoFilesOnArrival  | Video Dateien                                    |
| PlayCDAudioOnArrival     | AudioCD (Redbook Format CD mit Audiospuren) |
| PlayDVDMovieOnArrival    | DVD-Filme                                     |



 

In Windows Vista sind zusätzlich zu den oben aufgeführten Event andlers vordefiniert. 

| Eventhandlers-Schlüssel              | Medien-oder Dateityp   |
|--------------------------------|----------------------|
| PlaySuperVideoCDMovieOnArrival | Super VideoCD-Filme |
| PlayVideoCDMovieOnArrival      | VideoCD-Filme       |



 

 

 



