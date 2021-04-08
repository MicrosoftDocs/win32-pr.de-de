---
title: Beispiel für Registrierungs Werte
description: Das folgende Beispiel zeigt mögliche Daten für einige der Registrierungs Werte für das Authentifizierungsprotokoll.
ms.assetid: 07772af0-db56-4cc6-ad72-cf79d3813883
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bcbc3d4ca10a3e9298177a5eea240d0d34ade04
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2019
ms.locfileid: "104038400"
---
# <a name="registry-values-example"></a>Beispiel für Registrierungs Werte

Das folgende Beispiel zeigt mögliche Daten für einige der Registrierungs Werte für das Authentifizierungsprotokoll.

```
HKEY_LOCAL_MACHINE
   System
      CurrentControlSet
         Services
            Rasman
               PPP
                  EAP
                     40
                        Path
                        FriendlyName
                        ConfigUIPath
                        IdentityPath
                        InteractiveUIPath
                        RequireConfigUI
                        ConfigCLSID
                        StandaloneSupported
```



| Schlüsselname            | Datentyp        | Wert                                  |
|---------------------|-----------------|----------------------------------------|
| Pfad                | REG \_ Expand \_ SZ | % Systemroot% \\ system32 \\sample.dll     |
| FriendlyName        | REG- \_ SZ         | EAP-Beispiel Protokoll                    |
| Configuipath        | REG \_ Expand \_ SZ | % Systemroot% \\ system32 \\sample.dll     |
| Identitypath        | REG \_ Expand \_ SZ | % Systemroot% \\ system32 \\sample.dll     |
| Interactiveuipath   | REG \_ Expand \_ SZ | % Systemroot% \\ system32 \\sample.dll     |
| Requirements configui     | REG \_ DWORD      | 1                                      |
| Configclsid         | REG- \_ SZ         | {0000031a-0000-0000-C000-000000000046} |
| Standalonesupportiert | REG \_ DWORD      | 1                                      |



 

 

 




