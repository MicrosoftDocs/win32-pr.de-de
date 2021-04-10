---
title: Registrierungseinträge (com)
ms.assetid: f4f8875c-6416-4919-b49b-bcd675efcbd2
description: Weitere Informationen finden Sie in den Registrierungs Einträgen (com).
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 368e9eb5e4c2174c5b4b90df6586b58135085c5b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127569"
---
# <a name="registry-entries-com"></a>Registrierungseinträge (com)

Registrierungs Werte in den folgenden Registrierungs Schlüsseln steuern Aspekte der com-Funktionalität:

-   [**HKEY \_ - \_ \\ Software \\ Klassen für lokale Computer**](hkey-local-machine-software-classes.md)
-   [**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ OLE**](hkey-local-machine-software-microsoft-ole.md)
-   [**HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows NT \\ CurrentVersion**](hkey-local-machine-software-microsoft-windows-nt-currentversion.md)

Ab Windows Server 2003 verwendet com nur das aktuelle Prozess Token, um zu entscheiden, auf welche Registrierungs Struktur zugegriffen werden soll, und nicht auf das Thread Token. Wenn com nicht auf die Benutzerprofil-Registrierungs Struktur zugreifen kann, wird auf die **System Struktur des \_ lokalen \_ \\ HKEY** -Computers zugegriffen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Registrierung](/windows/desktop/SysInfo/registry)
</dt> </dl>

 

 
