---
title: Deaktivieren von Remotedesktopdienste Features
description: Zur Erhöhung der Sicherheit können Sie Remotedesktopdienste Funktionen deaktivieren.
ms.assetid: 93505e3a-a4f8-4b94-8dbb-646140b6fa58
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f2f5534b062fe4e594d0400cf16adff4367af01
ms.sourcegitcommit: da6887b92d8ef51f6b3f0d9307632822e92a8648
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/01/2020
ms.locfileid: "103949297"
---
# <a name="disabling-remote-desktop-services-features"></a>Deaktivieren von Remotedesktopdienste Features

Um die Sicherheit zu erhöhen, können Sie Remotedesktopdienste Funktionen wie die Zwischenablage Umleitung und die Drucker Umleitung für Clients, die mit Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servern verbunden sind, deaktivieren, indem Sie das Remotedesktop ActiveX-Steuerelement verwenden.

**So deaktivieren Sie Remotedesktopdienste Features**

1.  Bearbeiten Sie die Registrierung des Client Computers, und fügen Sie die folgenden Schlüssel hinzu:

    -   **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Terminal Server \\ disableclipboardredirection**
    -   **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Terminal Server \\ disabledriveredirection**
    -   **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Terminal Server \\ disableprinterredirect**

2.  Legen Sie den Wert beider Schlüssel auf **reg \_ DWORD** 1 fest.

 

 




