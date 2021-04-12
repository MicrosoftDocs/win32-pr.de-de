---
description: Wenn Sie sich entscheiden, das Löschen in Ihrer Anwendung außer mithilfe des InkOverlay-Objekts zu implementieren, können Sie dazu eine der beiden folgenden Methoden verwenden.
ms.assetid: c05c7dbf-c3e0-42a7-a97e-bb9d9764209d
title: Löschen mithilfe des Stifts
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c9e71828e826f2d57dd21e57934e12c8de0be03
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393521"
---
# <a name="erasing-by-using-the-pen"></a>Löschen mithilfe des Stifts

Wenn Sie sich entscheiden, das Löschen in Ihrer Anwendung außer mithilfe des [**InkOverlay**](inkoverlay-class.md) -Objekts zu implementieren, können Sie dazu eine der beiden folgenden Methoden verwenden.

## <a name="using-the-tip-of-the-pen"></a>Verwenden der Spitze des Stifts

Die Spitze des Tablettstifts wird im Allgemeinen für Handschrift und Zeichen verwendet. der Tipp kann jedoch auch zum Löschen von frei Hand Eingaben verwendet werden. Zu diesem Zweck muss die Anwendung über einen Lösch Modus verfügen, den Benutzer verwenden können. Verwenden Sie in diesem Modus Treffer Tests, um zu bestimmen, über welche Hand Eingaben der Cursor bewegt wird. Sie können den Lösch Modus so festlegen, dass nur die frei Hand Eingaben, die der Cursor übergibt, oder ganze Striche, die den Cursor Cursor überschneiden, abhängig von Entwurfs-oder Funktions Überlegungen gelöscht werden.

Ein Beispiel für die Verwendung eines Lösch Modus zum Löschen von frei Hand Eingaben finden Sie [im Beispiel zur](ink-erasing-sample.md)frei Hand Löschung.

## <a name="using-the-top-of-the-pen"></a>Verwenden des oberen Rands des Stifts

Um das Löschen am oberen Rand des Tablettstifts zu implementieren, muss Ihre Anwendung nach einer Änderung im Cursor suchen. Um nach dem umgekehrten Cursor zu suchen, lauschen Sie auf das [**CursorInRange**](inkoverlay-cursorinrange.md) -Ereignis, um zu bestimmen, wann sich der Cursor innerhalb des Kontexts der Anwendung befindet. Wenn sich der Cursor in einem Bereich befindet, suchen Sie im [**Cursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) Objekt nach der [**invertierten**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcursor-get_inverted) Eigenschaft. Wenn die **invertierte** Eigenschaft auf **true** festgelegt ist, führen Sie einen Treffer Test durch Löschen Sie die frei Hand Eingaben oder Striche, die den Cursor Cursor überschneiden, je nach Entwurfs-oder Funktions Überlegungen.

Ein Beispiel für die Verwendung des oberen Rands zum Löschen von frei Hand Eingaben finden Sie im [Beispiel zur frei Hand Löschung.](ink-erasing-sample.md)

### <a name="determining-if-erasing-with-the-top-of-the-pen-is-enabled"></a>Es wird ermittelt, ob das Löschen mit dem oberen Rand des Stifts aktiviert ist.

Benutzer können den oberen Rand des Stifts zum Löschen von frei Hand Eingaben in Anwendungen verwenden, die für Tablet PC entwickelt wurden, wenn die jeweilige Hardware dies zulässt. Der Zugriff auf diese Funktionalität erfolgt über ein Kontrollkästchen im Gruppenfeld Stift Schaltflächen auf der Registerkarte Stift Optionen im Dialogfeld "Einstellungen" der Tablet-und Stift-Einstellungen. Überprüfen Sie den folgenden Registrierungs Unterschlüssel, um zu ermitteln, ob der Benutzer das Löschen für den oberen Rand des Stifts aktiviert hat:

`HKEY_CURRENT_USER\SOFTWARE\Microsoft\WISP\PEN\SysEventParameters`

Der `EraseEnable` Eintrag dieses unter Schlüssels ist vom Typ " **reg \_ DWORD**". Der Wert dieses Eintrags ist 1 für aktiviert oder 0 für deaktiviert. Andere Werte sind für die zukünftige Verwendung reserviert.

Wenn die Anwendung den oberen Rand des Stifts zum Löschen verwendet, sollten Sie den Wert des eraseenable-Eintrags überprüfen und Zwischenspeichern, wenn Folgendes gilt:

-   Ihre Anwendung wird gestartet.
-   Jedes Mal, wenn die Anwendung den Fokus erhält, nachdem der Fokus verloren ist

Verwenden Sie diesen zwischengespeicherten Wert, um das Verhalten der Anwendung entsprechend zu ändern.

Im folgenden C- \# Beispiel wird eine- `GetEraseEnabled` Methode definiert, die den Wert des `EraseEnable` Eintrags des `SysEventParameters` unter Schlüssels überprüft. Die- `GetEraseEnabled` Methode gibt **true** zurück, wenn der Wert des Eintrags 1 ist. gibt **false** zurück, wenn der Wert des Eintrags 0 ist, oder löst eine [InvalidOperationException](/dotnet/api/system.invalidoperationexception) -Ausnahme aus, wenn der Wert des Eintrags nicht 1 oder 0 ist. Die `GetEraseEnabled` Methode gibt den erwarteten Wert " **true** " zurück, wenn der Unterschlüssel oder der Eintrag nicht vorhanden ist.


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



 

 
