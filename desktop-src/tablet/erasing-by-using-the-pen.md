---
description: Wenn Sie das Löschen in Ihrer Anwendung implementieren möchten, anstatt das InkOverlay-Objekt zu verwenden, können Sie dazu eine der beiden folgenden Methoden verwenden.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Löschen mithilfe des Stifts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f96d7d281f4e94a4a53f7e99e83c38192ceb7d31fbf9ee643653a20b4836a7cd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119936570"
---
# <a name="erasing-by-using-the-pen"></a>Löschen mithilfe des Stifts

Wenn Sie das Löschen in Ihrer Anwendung implementieren möchten, anstatt das [**InkOverlay-Objekt**](inkoverlay-class.md) zu verwenden, können Sie dazu eine der beiden folgenden Methoden verwenden.

## <a name="using-the-tip-of-the-pen"></a>Verwenden des Stifttipps

Die Spitze des Tablettstifts wird in der Regel für Handschrift und Zeichnung verwendet. der Tipp kann jedoch auch zum Löschen von Ink verwendet werden. Dazu muss die Anwendung über einen Löschmodus verfügen, den Benutzer verwenden können. Verwenden Sie in diesem Modus Treffertests, um zu bestimmen, welche Ink-Daten der Cursor bewegt. Sie können den Löschmodus so festlegen, dass nur die Vom Cursor übergibte Ink-Funktion oder ganze Striche, die den Pfad des Cursors überschneiden, je nach Entwurf oder funktionalen Überlegungen gelöscht werden.

Ein Beispiel für die Verwendung eines Löschmodus zum Löschen von Ink finden Sie unter [Ink Erasing Sample](ink-erasing-sample.md).

## <a name="using-the-top-of-the-pen"></a>Verwenden des oberen Stifts

Um das Löschen mit dem oberen Bereich des Tablettstifts zu implementieren, muss Ihre Anwendung nach einer Änderung im Cursor suchen. Um nach dem invertierten Cursor zu suchen, lauschen Sie auf das [**CursorInRange-Ereignis,**](inkoverlay-cursorinrange.md) um zu bestimmen, wann sich der Cursor im Kontext Ihrer Anwendung befindet. Wenn sich der Cursor im Bereich befindet, suchen Sie im Cursorobjekt nach [**der Inverted-Eigenschaft.**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) [](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Wenn die **Inverted-Eigenschaft** **true ist,** führen Sie Treffertests durch, um zu bestimmen, welche Ink-Eigenschaft der Cursor bewegt. Löschen Sie je nach Entwurf oder funktionalen Überlegungen entweder die Ink- oder die Striche, die den Pfad des Cursors überschneiden.

Ein Beispiel für die Verwendung des oberen Stifts zum Löschen von Ink finden Sie unter [Ink Erasing Sample](ink-erasing-sample.md).

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a>Bestimmen, ob das Löschen mit dem oberen Stift aktiviert ist

Benutzer können die Oberseite des Stifts verwenden, um Ink in Anwendungen zu löschen, die für Tablet PC entwickelt wurden, wenn ihre spezielle Hardware dies zulässt. Auf diese Funktionalität wird über ein Kontrollkästchen im Gruppenfeld Stiftschaltflächen auf der Registerkarte Stiftoptionen des Dialogfelds Tablet und Stift Einstellungen Systemsteuerung zugegriffen. Um zu ermitteln, ob der Benutzer das Löschen für den oberen Teil des Stifts aktiviert hat, überprüfen Sie den folgenden Registrierungsunterschlüssel:

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

Der `EraseEnable` Eintrag dieses Unterschlüssels ist vom Typ **REG \_ DWORD.** Der Wert dieses Eintrags ist 1 für aktiviert oder 0 für deaktiviert. Andere Werte sind für die zukünftige Verwendung reserviert.

Wenn Ihre Anwendung zulässt, dass der obere Teil des Stifts zum Löschen verwendet wird, sollten Sie den Wert des Eintrags EraseEnable in folgenden Zeiten überprüfen und zwischenspeichern:

-   Ihre Anwendung wird gestartet.
-   Jedes Mal, wenn Ihre Anwendung den Fokus erhält, nachdem sie den Fokus verloren hat.

Verwenden Sie diesen zwischengespeicherten Wert, um das Verhalten Ihrer Anwendung entsprechend zu ändern.

Im folgenden \# C-Beispiel wird eine `GetEraseEnabled` Methode definiert, die den Wert des `EraseEnable` Eintrags des Unterschlüssels `SysEventParameters` überprüft. Die Methode gibt TRUE zurück, wenn der Wert des Eintrags 1 ist; gibt FALSE zurück, wenn der Wert des Eintrags 0 ist, oder löst eine `GetEraseEnabled`  [InvalidOperationException-Ausnahme](/dotnet/api/system.invalidoperationexception) aus, wenn der Wert des Eintrags nicht 1 oder 0 ist.  Die `GetEraseEnabled` -Methode gibt den erwarteten Wert **von TRUE zurück,** wenn entweder der Unterschlüssel oder der Eintrag nicht vorhanden ist.


```C++
private bool GetEraseEnabled()
{
    // 0 is disabled, 1 is enabled. The default is enabled
    const int Enabled = 1;
    const int Disabled = 0;
    const int DefaultValue = Enabled;

    // Constants for the registry subkey and the entry
    const string Subkey =
                @"SOFTWARE\Microsoft\WISP\PEN\SysEventParameters";
    const string KeyEntry = "EraseEnable";

    // Open the registry subkey.
    Microsoft.Win32.RegistryKey regKey =
        Microsoft.Win32.Registry.CurrentUser.OpenSubKey(Subkey);

    // Retrieve the value of the EraseEnable subkey entry. If either
    // the subkey or the entry does not exist, use the default value.
    object keyValue = (null == regKey) ? DefaultValue :
        regKey.GetValue(KeyEntry,DefaultValue);

    switch((int)keyValue)
    {
        case Enabled:
            // Return true if erasing on pen inversion is enabled. 
            return true;
        case Disabled:
            // Return false if erasing on pen inversion is disabled. 
            return false;
        default:
            // Otherwise, throw an exception. Do not assume this is
            // a Boolean value. Enabled and Disabled are the values
            // defined for this entry at this time. Other values are
            // reserved for future use.
            throw new InvalidOperationException(
                "Unexpected registry subkey value.");
    }
}
```



 

 
