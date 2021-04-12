---
title: Informations Benachrichtigungen
description: Bei den Verbindungs Zuständen, die als Running States bezeichnet werden, ist keine Aktion für den Benachrichtigungs Handler erforderlich, es sei denn, ein Fehler tritt auf
ms.assetid: 3f5ea9e0-f75a-4b02-a0dc-86cb5012c242
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6223c808309fcac3afc563f02c160412c80c88
ms.sourcegitcommit: dc13cc13522097188392392d85f99de48a213984
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/28/2020
ms.locfileid: "104472397"
---
# <a name="informational-notifications"></a>Informations Benachrichtigungen

Bei den [Verbindungs Zuständen](connection-states.md) , die als Running States bezeichnet werden, ist keine Aktion für den Benachrichtigungs Handler erforderlich, es sei denn, ein Fehler tritt auf Die Ausführung von Zuständen erfolgt bei den Teilen des Verbindungs Vorgangs, die RAS automatisch verarbeitet, z. b. beim Herstellen einer Verbindung mit den erforderlichen Geräten, beim Authentifizieren des Benutzers und beim Warten auf einen Rückruf vom Remote Server. Bei der Benachrichtigung handelt es sich lediglich um einen Fortschrittsbericht an den Client.

Der Client kann diese Informations Benachrichtigungen an den Benutzer übergeben. In einigen ausgelaufenden Zuständen möchte der Client möglicherweise zusätzliche Informationen anzeigen. Ein Benachrichtigungs Handler, der eine rascs \_ connectdevice-Benachrichtigung empfängt, kann beispielsweise die Funktion " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " aufrufen, um den Namen und den Typ des Geräts abzurufen, mit dem eine Verbindung hergestellt wird. Ein weiteres Beispiel ist, wenn der Client eine in rascs \_ projizierte Benachrichtigung empfängt. Dies tritt auf, wenn die RAS-Projektionsphase des Verbindungs Vorgangs abgeschlossen wurde. Der Client kann die Funktion " [**rasgetprojectioninfo**](/previous-versions/windows/embedded/ms897107(v=msdn.10)) " aufrufen, um zusätzliche Informationen über die Projektion zu erhalten. Der Client kann diese Informationen verwenden, um den Benutzer darüber zu benachrichtigen, welche Netzwerkprotokolle von dieser Verbindung verwendet werden können.

Sie sollten vermeiden, Code zu schreiben, der von der Reihenfolge oder dem Vorkommen bestimmter Informations Zustände abhängt, da dies zwischen den Plattformen variieren kann.

 

 




