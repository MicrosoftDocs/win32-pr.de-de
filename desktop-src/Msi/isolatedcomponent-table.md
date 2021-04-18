---
description: Jeder Datensatz der isolatedcomponent-Tabelle ordnet die in der Spalte Komponenten Anwendung angegebene Komponente \_ (i. a. exe) der Komponente zu, die in der freigegebenen Spalte der Komponente angegeben ist \_ (häufig eine freigegebene DLL).
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: Isolatedcomponent-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c3e6c5bdba6efc546a36e77fa793c0b397f6d5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343308"
---
# <a name="isolatedcomponent-table"></a>Isolatedcomponent-Tabelle

Jeder Datensatz der isolatedcomponent-Tabelle ordnet die in der Spalte Komponenten Anwendung angegebene Komponente \_ (i. a. exe) der Komponente zu, die in der freigegebenen Spalte der Komponente angegeben ist \_ (häufig eine freigegebene DLL). Die [isolatecomponents-Aktion](isolatecomponents-action.md) installiert eine Kopie der freigegebenen Komponente an \_ einem privaten Speicherort, der von der Komponenten Anwendung verwendet werden soll \_ . Dadurch wird die Komponenten \_ Anwendung von anderen Kopien von freigegebenen Komponenten isoliert \_ , die an einem freigegebenen Speicherort auf dem Computer installiert werden können. Siehe [isolierte Komponenten](isolated-components.md).

Um eine Komponente \_ zu verknüpfen, die mit mehreren Komponenten Anwendungen gemeinsam verwendet \_ wird, fügen Sie für jedes Paar in der isolatedcomponents-Tabelle einen separaten Datensatz ein. Das Installationsprogramm kopiert die Dateien der \_ gemeinsam genutzten Komponenten in das Verzeichnis der einzelnen \_ installierten Komponenten Anwendungen.

Die isolatedcomponent-Tabelle weist die folgenden Spalten auf.



| Spalte                 | Typ                         | Schlüssel | Nullwerte zulässig |
|------------------------|------------------------------|-----|----------|
| Frei \_ gegebene Komponente      | [Bezeichner](identifier.md) | J   | N        |
| Komponenten \_ Anwendung | [Bezeichner](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Frei \_ gegebene Komponente
</dt> <dd>

Fremdschlüssel in der [Komponenten Tabelle](component-table.md). Die Komponente, die die freigegebene Datei enthält, normalerweise eine DLL. Die dll sollte die Schlüsseldatei für diese Komponente sein. Dabei muss es sich um eine andere Komponente handeln als in der \_ Spalte Komponenten Anwendung aufgeführt.

Die freigegebene Komponente steuert die Registrierung für alle isolierten Kopien der Komponente, und das Flag " **msidbcomponentattributesshareddllrefcount** " muss in der Spalte Attribute der Komponenten Tabelle festgelegt sein. Dadurch wird sichergestellt, dass das Installationsprogramm die Lebensdauer der freigegebenen Komponente verwalten kann.

</dd> <dt>

<span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>Komponenten \_ Anwendung
</dt> <dd>

Fremdschlüssel in der [Komponenten Tabelle](component-table.md). Die Komponente mit der exe-Datei, die die freigegebene Datei lädt. Die exe-Datei sollte die Schlüsseldatei für diese Komponente sein. Dabei muss es sich um eine andere Komponente handeln als in der freigegebenen Spalte der Komponente aufgeführt \_ .

</dd> </dl>

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE62](ice62.md)  
[ICE66](ice66.md)  
[ICE97](ice97.md)  
</dl>

 

 



