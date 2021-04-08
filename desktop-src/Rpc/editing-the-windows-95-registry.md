---
title: Bearbeiten der Windows 95-Registrierung
description: Sie können regedit verwenden, um die Windows 95-Registrierung zu bearbeiten und einen NSP zu bestimmen.
ms.assetid: 109daf4a-722f-4a25-a778-72360ee07ad9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c622ea44a5e365ca631d6d4db34af8e939ea6487
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103856772"
---
# <a name="editing-the-windows-95-registry"></a>Bearbeiten der Windows 95-Registrierung

Sie können regedit verwenden, um die Windows 95-Registrierung zu bearbeiten und einen NSP zu bestimmen.

**So bestimmen Sie einen Microsoft Locator Name Service Provider für Windows 95**

1.  Select

    **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **RPC**

2.  Erstellen Sie einen neuen Schlüssel mit dem Namen

    **NameService**

3.  Wenn Sie den **Nameservice** -Schlüssel ausgewählt haben, erstellen Sie die neuen **StringValue** -Namen, und ändern Sie Sie so, dass Sie Daten enthalten, wie in der folgenden Tabelle

    

    | Name                     | Daten                                                                        |
    |--------------------------|-----------------------------------------------------------------------------|
    | **Defaultsyntax**        | 3<br/>                                                                |
    | **Protokoll**             | ncacn \_ NP<br/>                                                        |
    | **Endpunkt**             | \\\\pipelocator<br/>                                                  |
    | **NetworkAddress**       | MyServer (wobei MyServer der Name des Windows NT-Computers ist)<br/> |
    | **Servernetworkaddress** | MyServer<br/>                                                         |

    

     

Sie können regedit zum Bearbeiten der Windows 95-Registrierung verwenden, um einen DCE-CDs-NSP zu bestimmen.

**So legen Sie einen DCE CDs Name Service Provider für Windows 95 fest**

1.  Select

    **HKEY \_ Software für den lokalen \_ Computer** \\  \\ **Microsoft** \\ **RPC**

2.  Erstellen Sie einen neuen Schlüssel mit dem Namen

    **NameService**

3.  Wenn Sie den **Nameservice** -Schlüssel ausgewählt haben, erstellen Sie die neuen **StringValue** -Namen, und ändern Sie Sie so, dass Sie Daten enthalten, wie in der folgenden Tabelle

    

    | Name                     | Daten                                                             |
    |--------------------------|------------------------------------------------------------------|
    | **Defaultsyntax**        | 3<br/>                                                     |
    | **Protokoll**             | ncacn \_ IP \_ TCP<br/>                                        |
    | **Endpunkt**             | "" (eine leere Zeichenfolge)<br/>                                  |
    | **NetworkAddress**       | MyServer (der Name des Host Computers, auf dem die nsid ausgeführt wird)<br/> |
    | **Servernetworkaddress** | MyServer (der Name des Host Computers, auf dem die nsid ausgeführt wird)<br/> |

    

     

    > [!Note]  
    > Zum Konfigurieren der DCE-CDs als Name Service Provider muss das Produkt "DCE-Zell Verzeichnisdienst" der Digital Equipment Corporation vorhanden sein. Weitere Informationen zu DCE CDs finden Sie in der Dokumentation der Digital Equipment Corporation.

     

 

 





