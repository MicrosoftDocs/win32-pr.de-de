---
description: In Windows 7 und höher können Sie den Unterschlüssel extendedsubcommandskey verwenden, um erweiterte Cascading Menüs zu erstellen.
ms.assetid: 6E8B4FB7-D4DB-4DBC-AF6F-59D02CB6AB13
title: Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "extendedsubcommandskey"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 220a38825ae250a0d58d30bc7de93f290f819eb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103756516"
---
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a>Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "extendedsubcommandskey"

In Windows 7 und höher können Sie den Unterschlüssel **extendedsubcommandskey** verwenden, um erweiterte Cascading Menüs zu erstellen.

Der folgende Screenshot zeigt ein Beispiel für ein erweitertes Cascading-Menü.

![Screenshot mit erweitertem Cascading-Menü für Geräte](images/file-assoc/extendedsubcommandskey.png)

Da **HKEY \_ Classes \_ root** eine Kombination aus **HKEY \_ Current \_ User** und **HKEY \_ local \_ Machine** ist, können Sie die subverben unter dem Unterschlüssel **HKEY \_ Current \_ User** \\ **Software** \\ **Classes** registrieren. Der Vorteil besteht darin, dass erhöhte Berechtigungen nicht erforderlich sind. Andere Dateizuordnungen können diese gesamte Gruppe von Verben wieder verwenden, indem Sie den gleichen **extendedsubcommandskey** -Unterschlüssel angeben. Wenn Sie diesen Versatz nicht wieder verwenden müssen, können Sie die Verben unter dem übergeordneten Element auflisten. Stellen Sie in diesem Fall sicher, dass der Standardwert des übergeordneten Elements leer ist. Dies wird im Beispiel zum Registrierungs Eintrag in diesem Abschnitt veranschaulicht.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Schritt 1:

Erstellen Sie einen Unterschlüssel unter **HKEY \_ Classes \_ root** \\ *ProgID* \\ **Shell** \\ *cascademenukey* , und geben Sie dem cascademenukey einen Namen, z.b. *caskadetten Test*. Fügen Sie dann einen MUIVerb-Eintrag des **reg \_ SZ** -Typs hinzu, und geben Sie ihm einen Namen wie z. b. Test Cascade Menu 2, wie im folgenden Registrierungs Beispiel veranschaulicht.

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a>Schritt 2:

Fügen Sie unter dem Unterschlüssel *caskadetten Test* , den Sie erstellt haben, einen Unterschlüssel **extendedsubcommandskey** hinzu, und fügen Sie dann die Dokument Unterbefehle (vom Typ **reg \_ SZ**) hinzu, z. b.:

```
HKEY_CLASSES_ROOT
   txtfile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Layout
               Properties
               Select all
```

Stellen Sie sicher, dass der Standardwert des unter Schlüssels *Test Cascade Menu 2* leer und als **(Wert nicht festgelegt)** angezeigt wird.

### <a name="step-3"></a>Schritt 3:

Füllen Sie die subverben mithilfe einer der folgenden statischen Verb Implementierungen auf. Beachten Sie, dass der commandflags-Unterschlüssel expcmdflags-Werte darstellt. Wenn Sie ein Trennzeichen vor oder nach dem kaskadierenden Menü Element hinzufügen möchten, verwenden Sie ECF \_ separatorbefore (0x20) oder ECF \_ separatorafter (0x40). Eine Beschreibung dieser Flags von Windows 7 und höher finden Sie unter [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags). ECF \_ separatorbefore funktioniert nur für Menü Elemente der obersten Ebene. MUIVerb ist vom Typ **reg \_ SZ**, und commandflags ist vom Typ **reg \_ DWORD**.

```
HKEY_CLASSES_ROOT
   txtile
      Shell
         Test Cascade Menu 2
            (Default)
            ExtendedSubCommandsKey
               Shell
                  cmd1
                     MUIVerb = Notepad
                     command
                        (Default) = %SystemRoot%\system32\notepad.exe %1
                  cmd2
                     MUIVerb = Wordpad
                     CommandFlags = 0x20
                     command
                        (Default) = C:\Program Files\Windows NT\Accessories\wordpad.exe %1
```

## <a name="remarks"></a>Bemerkungen

Der folgende Screenshot zeigt eine Abbildung der vorherigen Beispiele für den Registrierungsschlüssel Eintrag.

![Screenshot mit einem Beispiel für ein kaskadieres Menü, das die Auswahl von Editor und WordPad anzeigt](images/file-assoc/testcascademenu2.png)

 

 



