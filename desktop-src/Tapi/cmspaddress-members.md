---
description: In der folgenden Liste sind die CMSP-adressmember enthalten.
ms.assetid: ef15adef-1f4d-4bfc-8362-97fe1d118204
title: Cmspaddress-Member
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83213646427e7379b3eb2b45a0670f7908877175
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869200"
---
# <a name="cmspaddress-members"></a>Cmspaddress-Member



| Elementtypen                    | Name                    | BESCHREIBUNG                                                                                      |
|---------------------------------|-------------------------|--------------------------------------------------------------------------------------------------|
| Iunknown                        | \*Mio. \_ pftm               | Zeiger auf den Free Threaded Marshaller.                                                         |
| HANDLE                          | m \_ htevent              | Handle für Tapi3.dll-Ereignis, das verwendet wird, um TAPI darüber zu benachrichtigen, dass der MSP Daten an ihn senden möchte. |
| \_Eintrag auflisten                     | m \_ EventList            | Die Liste der Ereignisse.                                                                                  |
| Cmspcritsection                 | m \_ eventdatalock        | Die Sperre, die die Daten im Zusammenhang mit der Ereignis Behandlung mit TAPI schützt.                             |
| Itterminalmanager               | \*m \_ pitterminalmanager | Der Zeiger auf das Terminal-Manager-Objekt.                                                      |
| Cmsparray <itterminal \*> | m- \_ Terminals            | Die Liste der statischen Terminals, die für die Adresse verwendet werden können.                                    |
| BOOL                            | m- \_ terminalsuptag   | Dieses Flag ist **true** , wenn die Terminal Liste auf dem neuesten Stand ist.                                        |
| Cmspcritsection                 | m \_ terminaldatalock     | Die Sperre, die die Terminal bezogenen Datenmember schützt.                                        |



 

 

 



