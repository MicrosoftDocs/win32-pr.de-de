---
description: Die BindImage-Tabelle enthält Informationen zu jeder ausführbaren Datei oder dll, die an die von ihr importierten DLLs gebunden werden muss.
ms.assetid: 68bf064c-dd85-4796-8e08-6af307f94ad8
title: BindImage-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f47b97efc8886d7748d0426a49ed76567810939c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959502"
---
# <a name="bindimage-table"></a>BindImage-Tabelle

Die BindImage-Tabelle enthält Informationen zu jeder ausführbaren Datei oder dll, die an die von ihr importierten DLLs gebunden werden muss.

Die BindImage-Tabelle weist die folgenden Spalten auf.



| Spalte | Typ                         | Schlüssel | Nullwerte zulässig |
|--------|------------------------------|-----|----------|
| Datei\_ | [Bezeichner](identifier.md) | J   | N        |
| Pfad   | [Paths](paths.md)           | N   | J        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="File_"></span><span id="file_"></span><span id="FILE_"></span>Datei\_
</dt> <dd>

Ein externer Schlüssel für die Spalte einer der [Datei Tabellen](file-table.md). Dabei muss es sich um eine ausführbare Datei oder eine DLL-Datei handeln.

</dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>ADS
</dt> <dd>

Eine durch Semikolons getrennte Liste von Pfaden, die die Pfade darstellen, die durchsucht werden sollen, um die importierten DLLs zu suchen. Die Liste ist normalerweise eine Liste von Eigenschaften, wobei jede Eigenschaft in eckige Klammern () eingeschlossen ist \[ \] .

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Das Installationsprogramm berechnet die virtuelle Adresse der einzelnen Funktionen, die aus allen DLLs importiert werden, und die berechnete virtuelle Adresse wird dann in der Import Adress Tabelle (IAT) des importierten Images gespeichert.

Diese Tabelle wird beim Ausführen der [BindImage-Aktion](bindimage-action.md) bezeichnet.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE46](ice46.md)  
[ICE76](ice76.md)  
</dl>

 

 



