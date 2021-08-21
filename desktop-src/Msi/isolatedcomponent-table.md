---
description: Jeder Datensatz der IsolatedComponent-Tabelle ordnet die in der Spalte Komponentenanwendung angegebene Komponente (in der Regel eine .exe) der Komponente zu, die in der Spalte Freigegebene Komponenten (im Allgemeinen eine freigegebene DLL) angegeben \_ \_ ist.
ms.assetid: dc30e4c7-a938-4060-be4f-744de9c20fd9
title: IsolatedComponent-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9644f1e122464e1321d55c0b615892167e84a7e059472adc4f01ee6bac571720
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117805618"
---
# <a name="isolatedcomponent-table"></a>IsolatedComponent-Tabelle

Jeder Datensatz der IsolatedComponent-Tabelle ordnet die in der Spalte Komponentenanwendung angegebene Komponente (in der Regel eine .exe) der Komponente zu, die in der Spalte Freigegebene Komponenten (im Allgemeinen eine freigegebene DLL) angegeben \_ \_ ist. Die [Aktion IsolateComponents](isolatecomponents-action.md) installiert eine Kopie der Komponente Freigegeben an einem privaten Speicherort \_ zur Verwendung durch die \_ Komponentenanwendung. Dadurch wird die Komponentenanwendung von anderen Kopien der Freigegebenen Komponente isoliert, die an einem freigegebenen Speicherort auf dem \_ \_ Computer installiert werden können. Weitere Informationen [finden Sie unter Isolierte Komponenten.](isolated-components.md)

Um eine freigegebene Komponente mit mehreren Komponentenanwendung zu verknüpfen, fügen Sie einen separaten Datensatz für jedes Paar in die \_ \_ Tabelle IsolatedComponents ein. Das Installationsprogramm kopiert die Dateien von Component \_ Shared in das Verzeichnis jeder installierten \_ Komponentenanwendung.

Die Tabelle IsolatedComponent enthält die folgenden Spalten.



| Spalte                 | Typ                         | Key | Nullwerte zulässig |
|------------------------|------------------------------|-----|----------|
| Freigegebene \_ Komponente      | [Identifier](identifier.md) | J   | N        |
| \_Komponentenanwendung | [Identifier](identifier.md) | J   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="Component_Shared"></span><span id="component_shared"></span><span id="COMPONENT_SHARED"></span>Freigegebene \_ Komponente
</dt> <dd>

Fremdschlüssel in der [Komponententabelle](component-table.md). Die Komponente, die die freigegebene Datei enthält, in der Regel eine DLL. Die DLL sollte die Schlüsseldatei für diese Komponente sein. Dies muss eine andere Komponente sein als in der Spalte \_ Komponentenanwendung aufgeführt.

Die freigegebene Komponente steuert die Registrierung für alle isolierten Kopien der Komponente und muss das **Flag msidbComponentAttributesSharedDllRefCount** in der Spalte Attribute der Component-Tabelle festgelegt haben. Dadurch wird sichergestellt, dass das Installationsprogramm die Lebensdauer der freigegebenen Komponente verwalten kann.

</dd> <dt>

<span id="Component_Application"></span><span id="component_application"></span><span id="COMPONENT_APPLICATION"></span>\_Komponentenanwendung
</dt> <dd>

Fremdschlüssel in der [Komponententabelle](component-table.md). Die Komponente, die die Datei enthält.exe die die freigegebene Datei lädt. Die .exe sollte die Schlüsseldatei für diese Komponente sein. Dies muss eine andere Komponente sein als in der Spalte Freigegebene \_ Komponente aufgeführt.

</dd> </dl>

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
[ICE06](ice06.md)  
[ICE32](ice32.md)  
[ICE62](ice62.md)  
[ICE66](ice66.md)  
[ICE97](ice97.md)  
</dl>

 

 



