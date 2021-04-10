---
description: Mit der Aktion "Write-Environment Strings" werden die Werte von Umgebungsvariablen geändert.
ms.assetid: a91c1ffe-1bdd-49bb-aa6a-71667a1ed812
title: Aktion "Write Report Umgebungs Strings"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc3a9d64a1140fc883d94e8d3733608d29dc2d39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042494"
---
# <a name="writeenvironmentstrings-action"></a>Aktion "Write Report Umgebungs Strings"

Mit der Aktion "Write-Environment Strings" werden die Werte von Umgebungsvariablen geändert.

Umgebungsvariablen ändern sich nicht für die Installation, die ausgeführt wird, wenn die Aktion "Schreib Umgebungs Zeichenfolgen" oder " [removeenvironment Strings](removeenvironmentstrings-action.md) " ausgeführt wird. Unter Windows 2000, Windows Server 2003, Windows XP und Windows Vista werden diese Informationen in der Registrierung gespeichert, und es wird eine [**WM- \_ settingchange**](../winmsg/wm-settingchange.md) -Nachricht gesendet, um das System über die Änderungen zu benachrichtigen, wenn die Installation abgeschlossen ist. Ein anderer Prozess kann Benachrichtigungen über die Änderungen empfangen, indem er diese Nachrichten verarbeitet. Wenn ein Neustart des Systems aussteht, wird keine Nachricht gesendet. Ein Paket kann mithilfe der [**msisystemrebootpending**](msisystemrebootpending.md) -Eigenschaft überprüfen, ob ein Systemneustart aussteht.

Das Installationsprogramm führt die "Write Report Environment Strings"-Aktion nur während der Installation oder erneuten Installation einer Komponente aus und führt die [Aktion "removeumgebstrings](removeenvironmentstrings-action.md) " nur während des Entfernens einer Komponente aus.

Werte werden basierend auf der Auswahl der primären Aktionen und Modifizierer geschrieben oder entfernt. Diese werden im folgenden Abschnitt "Aktions Daten Meldungen" beschrieben. Beachten Sie, dass mit "Write-Environment Strings" abhängig von der angegebenen Aktion Variablen entfernt werden können und dass removeumgebungszeichenfolgen diese basierend auf der Erstellung der [Umgebungs Tabelle](environment-table.md)hinzufügen können.

## <a name="sequence-restrictions"></a>Sequenz Einschränkungen

Die [InstallValidate-Aktion](installvalidate-action.md) muss vor der removeumgebstrings-Aktion ausgeführt werden. Da die Aktion "Schreiben von Schreib Aktionen" und "removeumgebstrings" während einer Installation oder Entfernung einer Komponente nie angewendet werden, ist die relative Sequenz nicht eingeschränkt.

## <a name="actiondata-messages"></a>Aktions Daten Meldungen



| Feld | Beschreibung der Aktions Daten                                                                                                                                                                                                  |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[1\] | Der Name der zu ändernden Umgebungsvariablen.                                                                                                                                                                                 |
| \[2\] | Der Umgebungsvariablen Wert.                                                                                                                                                                                             |
| \[3\] | Hierbei handelt es sich um ein Bitflags-Feld, das die auszuführende Aktion angibt. Fügen Sie nur ein Bit für eine primäre Aktion ein. In diesem Feld sind möglicherweise mehrere modifiziererbits enthalten. Weitere Informationen finden Sie in den folgenden Bitflag-Beschreibungen. |



 



| Bitwert | Beschreibung der primären Aktionen                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x1       | Festlegen. Legt den Wert der Umgebungsvariablen in allen Fällen fest.<br/> Wenn dieses Bit mit einem Anfüge-oder Präfix-modifiziererbit kombiniert wird, wird der Wert durch die Aktion zu einem beliebigen vorhandenen Wert in der Variablen hinzugefügt.<br/> |
| 0x2       | Festlegen. Legt den Wert fest, wenn die Variable nicht vorhanden ist.<br/> Wenn dieses Bit mit einem Anfüge-oder Präfix-modifiziererbit kombiniert wird, wird der Wert durch die Aktion zu einem beliebigen vorhandenen Wert in der Variablen hinzugefügt.<br/>                |
| 0x4       | Entfernen Entfernt den Wert aus der Variablen.<br/> Wenn dieses Bit mit einem Anfüge-oder Präfix-modifiziererbit kombiniert wird, wird der Wert aus der vorhandenen Zeichenfolge entfernt, wenn der Wert vorhanden ist.<br/>               |



 



| Bitwert  | Beschreibung des Modifizierers                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0x20000000 | Wenn dieses Bit festgelegt ist, werden Aktionen auf die Umgebungsvariablen des Computers angewendet.<br/> Wenn dieses Bit nicht festgelegt ist, werden Aktionen auf die Umgebungsvariablen des Benutzers angewendet.<br/> |
| 0x40000000 | Anfügen. Dieses Bit ist optional. Legen Sie nicht die Anfüge-und Präfix Modifizierer fest.<br/>                                                                                            |
| 0x80000000 | Vorsatz. Dieses Bit ist optional. Legen Sie nicht die Anfüge-und Präfix Modifizierer fest.<br/>                                                                                            |



 

 

 
