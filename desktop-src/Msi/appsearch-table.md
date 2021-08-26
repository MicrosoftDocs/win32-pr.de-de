---
description: Die Tabelle AppSearch enthält Eigenschaften, die für die Suche nach einer Datei mit einer bestimmten Dateisignatur erforderlich sind. Die AppSearch-Tabelle kann auch verwendet werden, um eine Eigenschaft auf den vorhandenen Wert einer Registrierung oder .ini Dateieintrags festzulegen.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: AppSearch-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 450ab07a397366ca01e664b88321942e4f6a7800cd9e04c4d0cbbe048eed8b87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045650"
---
# <a name="appsearch-table"></a>AppSearch-Tabelle

Die Tabelle AppSearch enthält Eigenschaften, die für die Suche nach einer Datei mit einer bestimmten Dateisignatur erforderlich sind. Die AppSearch-Tabelle kann auch verwendet werden, um eine Eigenschaft auf den vorhandenen Wert einer Registrierung oder .ini Dateieintrags festzulegen.

Die Tabelle AppSearch enthält die folgenden Spalten.



| Spalte      | Typ                         | Key | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Eigenschaft    | [Identifier](identifier.md) | J   | N        |
| Signatur\_ | [Identifier](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Eigenschaft
</dt> <dd>

Wenn Sie die [AppSearch-Aktion](appsearch-action.md) ausführen, wird diese Eigenschaft auf den Speicherort der Datei festgelegt, die durch die Spalte Signatur angegeben \_ wird. Diese Eigenschaft wird festgelegt, wenn die Dateisignatur auf dem Computer des Benutzers vorhanden ist. Die in dieser Spalte verwendeten Eigenschaften müssen [öffentliche](public-properties.md) Eigenschaften sein und einen Bezeichner aufweisen, der keine Kleinbuchstaben enthält.

Die im Feld Eigenschaft aufgeführte Eigenschaft kann in der [Tabelle Property](property-table.md) oder über eine Befehlszeile initialisiert werden. Wenn die [AppSearch-Aktion](appsearch-action.md) die Signatur findet, überschreibt das Installationsprogramm den initialisierten Eigenschaftswert mit dem gefundenen Wert. Wenn die Signatur nicht gefunden wird, wird der anfängliche Eigenschaftswert verwendet. Wenn die Eigenschaft nie initialisiert wurde, wird die Eigenschaft nur festgelegt, wenn die Signatur gefunden wird. Andernfalls ist die Eigenschaft nicht definiert.

</dd> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Signatur\_
</dt> <dd>

Die Spalte Signatur \_ enthält einen eindeutigen Bezeichner namens Signatur und ist auch ein externer Schlüssel in den Tabellen [RegLocator,](reglocator-table.md) [IniLocator,](inilocator-table.md) [CompLocator](complocator-table.md)und [DrLocator.](drlocator-table.md) Bei der Suche nach einer Datei muss der Wert in dieser Spalte auch ein Fremdschlüssel in der [Signaturtabelle](signature-table.md) sein. Wenn der Wert in dieser Spalte nicht in der Signaturtabelle aufgeführt ist, ermittelt das Installationsprogramm, dass die Suche nach einem Verzeichnis erfolgt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die [AppSearch-Aktion](appsearch-action.md) in [*Sequenztabellen*](s-gly.md) verarbeitet die Informationen in dieser Tabelle. Informationen zur Verwendung von *Sequenztabellen* finden Sie unter [Verwenden einer Sequenztabelle.](using-a-sequence-table.md)

Die [AppSearch-Aktion](appsearch-action.md) sucht zuerst mithilfe der [CompLocator-Tabelle,](complocator-table.md) der [RegLocator-Tabelle](reglocator-table.md) zweiten, der [IniLocator-Tabelle](inilocator-table.md) und schließlich der [DrLocator-Tabelle](drlocator-table.md) nach Signaturen. Dateisignaturen sind in der [Signaturtabelle](signature-table.md) aufgeführt. Eine Signatur, die sich nicht in der Signaturtabelle befindet, kennzeichnet ein Verzeichnis, und die Aktion legt die -Eigenschaft auf den Verzeichnispfad für diese Signatur fest.

Weitere Informationen finden Sie unter [Suchen nach vorhandenen Anwendungen, Dateien, Registrierungseinträgen oder .ini Dateieinträgen.](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE52](ice52.md)  
[ICE88](ice88.md)  
</dl>

 

 



