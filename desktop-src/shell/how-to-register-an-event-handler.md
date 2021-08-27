---
description: Ein Gerät kann potenziell viele Ereignisse generieren, und jedes Ereignis hat die Möglichkeit, von einem von mehreren verschiedenen Handlern behandelt zu werden.
ms.assetid: C203B5AB-917C-4543-98D6-EDE02E0B5E49
title: Registrieren eines Ereignishandlers
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f96aedc8b6b7944238938539a8fafa5d80c6dc7f1afd4dc5f818ecc91abd08c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120090560"
---
# <a name="how-to-register-an-event-handler"></a>Registrieren eines Ereignishandlers

Ein Gerät kann potenziell viele Ereignisse generieren, und jedes Ereignis hat die Möglichkeit, von einem von mehreren verschiedenen Handlern behandelt zu werden. In Windows XP werden die folgenden Ereignisse definiert:

-   DeviceArrarrarr
-   DeviceRemoval
-   MediaArrarrarr
-   MediaRemoval

## <a name="instructions"></a>Anweisungen


Ereignishandler werden unter dem **EventHandlers-Schlüssel** definiert. Die Werte eines Ereignishandlerschlüssels sind die Namen der einzelnen Handler, aus denen der Benutzer auswählen muss, wenn das Ereignis erkannt wird. Diesen Einträgen ist kein Datenwert zugeordnet. Im Folgenden finden Sie eine Beispieldefinition für einen benutzerdefinierten Ereignishandler namens **MyNewRemovalEventHandler,** der dem Benutzer diese Handlermöglichkeiten bietet:

-   Ein Handler, der verwendet werden soll, wenn das Ereignis auf einem Gerät erkannt wird, das von dem Unternehmen namens Contoso, Inc. erstellt wurde.
-   Ein Handler, der verwendet werden soll, wenn das Ereignis auf einem Gerät erkannt wird, das von dem Unternehmen namens Fabrikam, Inc. hergestellt wurde.
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

Nachdem ein Ereignishandler definiert wurde, muss er für eine der Ereignismöglichkeiten bei einem Gerätehandler registriert werden: DeviceArrarr, DeviceRemoval, MediaArrhir oder MediaRemoval. Der zuvor definierte MyNewRemovalEventHandler wird für DeviceRemoval unter einem benutzerdefinierten Gerätehandler namens MyDeviceHandler verwendet und im folgenden Beispiel zu diesem Zweck definiert. Auch hier verfügt der Registrierungswert über keine Datenkomponente.

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

Windows XP definiert den folgenden Satz von EventHandlern. 

| EventHandlers-Schlüssel        | Medien- oder Dateityp                             |
|--------------------------|------------------------------------------------|
| HandleCDBurningOnArrival | Leere CD-R/CD-RW                               |
| ShowPicturesOnArrival    | Bilddateien                                  |
| PlayMusicFilesOnArrival  | Musik Dateien                                    |
| PlayVideoFilesOnArrival  | Videodateien                                    |
| PlayCDAudioOnArrival     | Audio-CD (REDBOOK-Format: CD mit Audiospuren) |
| PlayDVDMovieOnArrival    | DVD-Filme                                     |



 

Windows Vista definiert den folgenden Satz von EventHandlern zusätzlich zu den oben genannten. 

| EventHandlers-Schlüssel              | Medien- oder Dateityp   |
|--------------------------------|----------------------|
| PlaySuperVideoCDMovieOnArrival | Super VideoCD movies |
| PlayVideoCDMovieOnArrival      | VideoCD-Filme       |



 

 

 



