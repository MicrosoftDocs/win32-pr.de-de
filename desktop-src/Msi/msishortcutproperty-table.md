---
description: Die Tabelle MsiShortcutProperty ermöglicht dem Fenster-Installer das Festlegen von Eigenschaften für Verknüpfungen, die auch Windows Shell-Objekten verwendet werden.
ms.assetid: d959769d-113f-4af2-89d4-ad3f5322de33
title: MsiShortcutProperty-Tabelle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7cf51d8016cdc87008a6cc9a20daee1f35131af7ea0f5827c67da7f45a6e46
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118944427"
---
# <a name="msishortcutproperty-table"></a>MsiShortcutProperty-Tabelle

Die Tabelle MsiShortcutProperty ermöglicht dem Fenster-Installer das Festlegen von Eigenschaften für Verknüpfungen, die auch Windows [Shell-Objekten verwendet](/previous-versions/windows/desktop/legacy/bb773177(v=vs.85)) werden. Ab Windows Vista und Windows Server 2008 stellt die Windows Shell eine IPropertyStore-Schnittstelle für Shellobjekte wie Verknüpfungen bereit. Ein Windows Installer 5.0-Paket, das auf Windows Server 2008 R2 oder Windows 7 ausgeführt wird, kann diese Eigenschaften festlegen, wenn die Verknüpfung installiert wird.

**[Windows Installer 4.5 oder früher:](not-supported-in-windows-installer-4-5.md)** Nicht unterstützt. Diese Tabelle ist ab Windows Installer 5.0 verfügbar.

Die Tabelle MsiShortcutProperty enthält die folgenden Spalten.



| Spalte              | Typ                         | Key | Nullwerte zulässig |
|---------------------|------------------------------|-----|----------|
| MsiShortcutProperty | [Identifier](identifier.md) | J   | N        |
| Verknüpfung\_          | [Identifier](identifier.md) | N   | N        |
| PropertyKey         | [Formatiert](formatted.md)   | N   | N        |
| PropVariantValue    | [Formatiert](formatted.md)   | N   | N        |



 

## <a name="columns"></a>Spalten

<dl> <dt>

<span id="MsiShortcutProperty"></span><span id="msishortcutproperty"></span><span id="MSISHORTCUTPROPERTY"></span>MsiShortcutProperty
</dt> <dd>

Eindeutiger Bezeichner für diese Zeile der Tabelle MsiShortcutProperty.

</dd> <dt>

<span id="Shortcut_"></span><span id="shortcut_"></span><span id="SHORTCUT_"></span>Verknüpfung\_
</dt> <dd>

Ein Schlüssel in der [Verknüpfungstabelle,](shortcut-table.md) der die Verknüpfung identifiziert, für die eine Eigenschaft festgelegt ist.

</dd> <dt>

<span id="PropertyKey"></span><span id="propertykey"></span><span id="PROPERTYKEY"></span>PropertyKey
</dt> <dd>

Ein Zeichenfolgenwert, der Informationen für die [**PROPERTYKEY-Struktur**](/windows/win32/api/wtypes/ns-wtypes-propertykey) enthält. Die Informationen in diesem Feld müssen auf den kanonischen Namen einer Eigenschaft verweisen, die beim Windows registriert ist. Weitere Informationen zum Eigenschaftensystem Windows Eigenschaftensystem finden Sie unter [Übersicht über das Eigenschaftensystem.](/previous-versions//bb776909(v=vs.85))

</dd> <dt>

<span id="PropVariantValue"></span><span id="propvariantvalue"></span><span id="PROPVARIANTVALUE"></span>PropVariantValue
</dt> <dd>

Ein Zeichenfolgenwert, der Informationen für die [**PROPVARIANT-Struktur**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) enthält.

</dd> </dl>

Für eine Verknüpfung können mehrere Eigenschaften festgelegt werden. Wenn dieselbe Eigenschaft mehrmals für dieselbe Verknüpfung festgelegt wird, wird der Wert in einer nicht angegebenen Reihenfolge festgelegt.

Windows Das Installationsprogramm kann Tastenkombinationseigenschaften nur festlegen, wenn die Verknüpfung installiert oder neu installiert wird. Ein Patch, bei dem eine bereits installierte Verknüpfung nicht neu installiert wird, aktualisiert die Eigenschaften der Verknüpfung nicht. Ein Patch kann die Eigenschaften aktualisieren, indem eine [Verknüpfungstabelle](shortcut-table.md) in das Patchpaket ein- und die Verknüpfung neu installiert wird.

## <a name="remarks"></a>Hinweise

[Windows Installer-Fehlermeldung](windows-installer-error-messages.md) 1946 wird als Warnung zurückgegeben, und die Installation wird fortgesetzt, wenn Windows Installer keine in der Tabelle MsiShortcutProperty angegebene Shortcuteigenschaft festlegen kann.

## <a name="validation"></a>Überprüfung

<dl>

[ICE03](ice03.md)  
</dl>

 

 
