---
description: Die AppSearch-Tabelle enthält die Eigenschaften, die für die Suche nach einer Datei mit einer bestimmten Datei Signatur erforderlich sind. Die AppSearch-Tabelle kann auch verwendet werden, um eine Eigenschaft auf den vorhandenen Wert eines Registrierungs-oder INI-Datei Eintrags festzulegen.
ms.assetid: d560096f-6baa-4fea-8786-f4e3d5ee6bf4
title: AppSearch-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9419a768a51364b4f22444288e6728a87289aa0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215717"
---
# <a name="appsearch-table"></a>AppSearch-Tabelle

Die AppSearch-Tabelle enthält die Eigenschaften, die für die Suche nach einer Datei mit einer bestimmten Datei Signatur erforderlich sind. Die AppSearch-Tabelle kann auch verwendet werden, um eine Eigenschaft auf den vorhandenen Wert eines Registrierungs-oder INI-Datei Eintrags festzulegen.

Die AppSearch-Tabelle weist die folgenden Spalten auf.



| Spalte      | Typ                         | Schlüssel | Nullwerte zulässig |
|-------------|------------------------------|-----|----------|
| Eigenschaft    | [Bezeichner](identifier.md) | J   | N        |
| Signatur\_ | [Bezeichner](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Property"></span><span id="property"></span><span id="PROPERTY"></span>Property
</dt> <dd>

Durch das Ausführen der [AppSearch](appsearch-action.md) -Aktion wird diese Eigenschaft auf den Speicherort der Datei festgelegt, der in der Signatur Spalte angegeben ist \_ . Diese Eigenschaft wird festgelegt, wenn die Datei Signatur auf dem Computer des Benutzers vorhanden ist. Die in dieser Spalte verwendeten Eigenschaften müssen [öffentliche](public-properties.md) Eigenschaften sein und über einen Bezeichner verfügen, der keine Kleinbuchstaben enthält.

Die im Eigenschaften Feld aufgelistete Eigenschaft kann in der [Eigenschaften](property-table.md) Tabelle oder über die Befehlszeile initialisiert werden. Wenn die [AppSearch](appsearch-action.md) -Aktion die Signatur sucht, überschreibt der Installer den initialisierten Eigenschafts Wert mit dem gefundenen Wert. Wenn die Signatur nicht gefunden wird, wird der anfängliche Eigenschafts Wert verwendet. Wenn die Eigenschaft nie initialisiert wurde, wird die Eigenschaft nur festgelegt, wenn die Signatur gefunden wurde. Andernfalls ist die Eigenschaft nicht definiert.

</dd> <dt>

<span id="Signature_"></span><span id="signature_"></span><span id="SIGNATURE_"></span>Unter\_
</dt> <dd>

Die \_ Spalte Signatur enthält einen eindeutigen Bezeichner, der als Signatur bezeichnet wird, und ist auch ein externer Schlüssel in den Tabellen [reglocator](reglocator-table.md), [inilocator](inilocator-table.md), [complocator](complocator-table.md)und [drlocator](drlocator-table.md) . Wenn Sie nach einer Datei suchen, muss der Wert in dieser Spalte auch ein Fremdschlüssel in der [Signatur](signature-table.md) Tabelle sein. Wenn der Wert in dieser Spalte nicht in der Signatur Tabelle aufgeführt ist, ermittelt das Installationsprogramm, dass die Suche nach einem Verzeichnis erfolgt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Die [AppSearch](appsearch-action.md) -Aktion in [*Sequenz Tabellen*](s-gly.md) verarbeitet die Informationen in dieser Tabelle. Weitere Informationen zum Verwenden von *Sequenz Tabellen* finden Sie unter [Verwenden einer Sequenz Tabelle](using-a-sequence-table.md).

Die [AppSearch](appsearch-action.md) -Aktion sucht mithilfe der Tabelle " [complocator](complocator-table.md) " zuerst nach Signaturen, der Tabelle " [reglocator](reglocator-table.md) ", der zweiten Tabelle, der Tabelle " [inilocator](inilocator-table.md) " und schließlich der Tabelle " [drlocator](drlocator-table.md) ". Datei Signaturen werden in der [Signatur](signature-table.md) Tabelle aufgeführt. Eine Signatur, die nicht in der Signatur Tabelle ist, gibt ein Verzeichnis an, und die-Eigenschaft legt die-Eigenschaft auf den Verzeichnispfad für diese Signatur fest.

Weitere Informationen finden Sie [untersuchen nach vorhandenen Anwendungen, Dateien, Registrierungs Einträgen oder INI-Datei Einträgen](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE52](ice52.md)  
[ICE88](ice88.md)  
</dl>

 

 



