---
description: Die msishortcutproperty-Tabelle ermöglicht dem Fenster Installer das Festlegen von Eigenschaften für Tastenkombinationen, die auch als Windows-Shellobjekte dienen.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: Msishortcutproperty-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f295feabd6ff9b1677fdcf47791959b0fbb8a920
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529798"
---
# <a name="msishortcutproperty-table"></a>Msishortcutproperty-Tabelle

Die msishortcutproperty-Tabelle ermöglicht dem Fenster Installer das Festlegen von Eigenschaften für Tastenkombinationen, die auch als [Windows-Shellobjekte](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) dienen. Ab Windows Vista und Windows Server 2008 bietet die Windows-Shell eine IPropertyStore-Schnittstelle für Shellobjekte wie z. b. Verknüpfungen. Mit einem Windows Installer 5,0-Paket, das unter Windows Server 2008 R2 oder Windows 7 ausgeführt wird, können diese Eigenschaften festgelegt werden, wenn die Verknüpfung installiert wird.

**[Windows Installer 4,5 oder früher](not-supported-in-windows-installer-4-5.md):** Nicht unterstützt. Diese Tabelle ist ab Windows Installer 5,0 verfügbar.

Die msishortcutproperty-Tabelle weist die folgenden Spalten auf.



| Spalte              | Typ                         | Schlüssel | Nullwerte zulässig |
|---------------------|------------------------------|-----|----------|
| Msishortcutproperty | [Bezeichner](identifier.md) | J   | N        |
| Abkürzung\_          | [Bezeichner](identifier.md) | N   | N        |
| PropertyKey         | [Großformatige](formatted.md)   | N   | N        |
| Propvariantvalue    | [Großformatige](formatted.md)   | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>Msishortcutproperty
</dt> <dd>

Eindeutiger Bezeichner für diese Zeile der msishortcutproperty-Tabelle.

</dd> <dt>

<span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Kontext\_
</dt> <dd>

Ein Schlüssel in die [Verknüpfungs Tabelle, der die](shortcut-table.md) Verknüpfung mit einem Eigenschaften Satz identifiziert.

</dd> <dt>

<span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey
</dt> <dd>

Ein Zeichen folgen Wert, der Informationen für die [**PropertyKey**](/windows/win32/api/wtypes/ns-wtypes-propertykey) -Struktur bereitstellt. Die Informationen in diesem Feld müssen auf den kanonischen Namen einer Eigenschaft verweisen, die beim Windows-Eigenschaften System registriert ist. Weitere Informationen zum Windows-Eigenschaften System finden Sie in der [Übersicht über das Eigenschaften System](/previous-versions//bb776909(v=vs.85)).

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>Propvariantvalue
</dt> <dd>

Ein Zeichen folgen Wert, der Informationen für die [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) -Struktur bereitstellt.

</dd> </dl>

Für eine Verknüpfung können mehrere Eigenschaften festgelegt werden. Wenn dieselbe Eigenschaft mehrmals bei derselben Verknüpfung festgelegt wird, wird der Wert in einer nicht angegebenen Reihenfolge festgelegt.

Windows Installer können die Verknüpfungs Eigenschaften nur festlegen, wenn die Verknüpfung installiert oder neu installiert wird. Bei einem Patch, bei dem eine bereits installierte Verknüpfung nicht neu installiert wird, werden die Eigenschaften der Verknüpfung nicht aktualisiert. Ein Patch kann die Eigenschaften aktualisieren, indem er [eine](shortcut-table.md) Verknüpfungs Tabelle in das Patchpaket einschließt und die Verknüpfung erneut installiert.

## <a name="remarks"></a>Bemerkungen

[Windows Installer Fehlermeldung](windows-installer-error-messages.md) 1946 wird als Warnung zurückgegeben, und die Installation wird fortgesetzt, wenn Windows Installer keine in der Tabelle msishortcutproperty angegebene Verknüpfungs Eigenschaft festlegen kann.

## <a name="validation"></a>Überprüfen

<dl>

[ICE03](ice03.md)  
</dl>

 

 
