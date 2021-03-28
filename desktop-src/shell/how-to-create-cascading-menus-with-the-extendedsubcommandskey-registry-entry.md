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
# <a name="how-to-create-cascading-menus-with-the-extendedsubcommandskey-registry-entry"></a><span data-ttu-id="f9d60-103">Erstellen von kaskadierenden Menüs mit dem Registrierungs Eintrag "extendedsubcommandskey"</span><span class="sxs-lookup"><span data-stu-id="f9d60-103">How to Create Cascading Menus with the ExtendedSubCommandsKey Registry Entry</span></span>

<span data-ttu-id="f9d60-104">In Windows 7 und höher können Sie den Unterschlüssel **extendedsubcommandskey** verwenden, um erweiterte Cascading Menüs zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f9d60-104">In Windows 7 and later, you can use the **ExtendedSubCommandsKey** subkey to create extended cascading menus.</span></span>

<span data-ttu-id="f9d60-105">Der folgende Screenshot zeigt ein Beispiel für ein erweitertes Cascading-Menü.</span><span class="sxs-lookup"><span data-stu-id="f9d60-105">The following screen shot is an example of an extended cascading menu.</span></span>

![Screenshot mit erweitertem Cascading-Menü für Geräte](images/file-assoc/extendedsubcommandskey.png)

<span data-ttu-id="f9d60-107">Da **HKEY \_ Classes \_ root** eine Kombination aus **HKEY \_ Current \_ User** und **HKEY \_ local \_ Machine** ist, können Sie die subverben unter dem Unterschlüssel **HKEY \_ Current \_ User** \\ **Software** \\ **Classes** registrieren.</span><span class="sxs-lookup"><span data-stu-id="f9d60-107">Because **HKEY\_CLASSES\_ROOT** is a combination of **HKEY\_CURRENT\_USER** and **HKEY\_LOCAL\_MACHINE**, you can register the subverbs under the **HKEY\_CURRENT\_USER**\\**Software**\\**Classes** subkey.</span></span> <span data-ttu-id="f9d60-108">Der Vorteil besteht darin, dass erhöhte Berechtigungen nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f9d60-108">The advantage of doing so is that elevated permission is not required.</span></span> <span data-ttu-id="f9d60-109">Andere Dateizuordnungen können diese gesamte Gruppe von Verben wieder verwenden, indem Sie den gleichen **extendedsubcommandskey** -Unterschlüssel angeben.</span><span class="sxs-lookup"><span data-stu-id="f9d60-109">Other file associations can reuse this entire set of verbs by specifying the same **ExtendedSubCommandsKey** subkey.</span></span> <span data-ttu-id="f9d60-110">Wenn Sie diesen Versatz nicht wieder verwenden müssen, können Sie die Verben unter dem übergeordneten Element auflisten.</span><span class="sxs-lookup"><span data-stu-id="f9d60-110">If you do not need to reuse this set of verbs, you can list the verbs under the parent.</span></span> <span data-ttu-id="f9d60-111">Stellen Sie in diesem Fall sicher, dass der Standardwert des übergeordneten Elements leer ist. Dies wird im Beispiel zum Registrierungs Eintrag in diesem Abschnitt veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f9d60-111">In this case, make sure the default value of the parent is empty, as illustrated in the registry entry example in this section.</span></span>

## <a name="instructions"></a><span data-ttu-id="f9d60-112">Instructions</span><span class="sxs-lookup"><span data-stu-id="f9d60-112">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="f9d60-113">Schritt 1:</span><span class="sxs-lookup"><span data-stu-id="f9d60-113">Step 1:</span></span>

<span data-ttu-id="f9d60-114">Erstellen Sie einen Unterschlüssel unter **HKEY \_ Classes \_ root** \\ *ProgID* \\ **Shell** \\ *cascademenukey* , und geben Sie dem cascademenukey einen Namen, z.b. *caskadetten Test*.</span><span class="sxs-lookup"><span data-stu-id="f9d60-114">Create a subkey under **HKEY\_CLASSES\_ROOT**\\*ProgID*\\**shell**\\*CascadeMenuKey* and give the CascadeMenuKey a name such as *CascadeTest*, for example.</span></span> <span data-ttu-id="f9d60-115">Fügen Sie dann einen MUIVerb-Eintrag des **reg \_ SZ** -Typs hinzu, und geben Sie ihm einen Namen wie z. b. Test Cascade Menu 2, wie im folgenden Registrierungs Beispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f9d60-115">Then add a MUIVerb entry of **REG\_SZ** type and give it a name such as Test Cascade Menu 2, as illustrated in the following registry example.</span></span>

```
HKEY_CLASSES_ROOT
   txtfile
      shell
         CascadeTest
            MUIVerb = Test Cascade Menu 2
```

### <a name="step-2"></a><span data-ttu-id="f9d60-116">Schritt 2:</span><span class="sxs-lookup"><span data-stu-id="f9d60-116">Step 2:</span></span>

<span data-ttu-id="f9d60-117">Fügen Sie unter dem Unterschlüssel *caskadetten Test* , den Sie erstellt haben, einen Unterschlüssel **extendedsubcommandskey** hinzu, und fügen Sie dann die Dokument Unterbefehle (vom Typ **reg \_ SZ**) hinzu, z. b.:</span><span class="sxs-lookup"><span data-stu-id="f9d60-117">Under the *CascadeTest* subkey that you created, add an **ExtendedSubCommandsKey** subkey, and then add the document subcommands (of type **REG\_SZ**); for example:</span></span>

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

<span data-ttu-id="f9d60-118">Stellen Sie sicher, dass der Standardwert des unter Schlüssels *Test Cascade Menu 2* leer und als **(Wert nicht festgelegt)** angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="f9d60-118">Ensure that the default value of the *Test Cascade Menu 2* subkey is empty, and shown as **(value not set)**.</span></span>

### <a name="step-3"></a><span data-ttu-id="f9d60-119">Schritt 3:</span><span class="sxs-lookup"><span data-stu-id="f9d60-119">Step 3:</span></span>

<span data-ttu-id="f9d60-120">Füllen Sie die subverben mithilfe einer der folgenden statischen Verb Implementierungen auf.</span><span class="sxs-lookup"><span data-stu-id="f9d60-120">Populate the subverbs using any of the following static verb implementations.</span></span> <span data-ttu-id="f9d60-121">Beachten Sie, dass der commandflags-Unterschlüssel expcmdflags-Werte darstellt.</span><span class="sxs-lookup"><span data-stu-id="f9d60-121">Note that the CommandFlags subkey represents EXPCMDFLAGS values.</span></span> <span data-ttu-id="f9d60-122">Wenn Sie ein Trennzeichen vor oder nach dem kaskadierenden Menü Element hinzufügen möchten, verwenden Sie ECF \_ separatorbefore (0x20) oder ECF \_ separatorafter (0x40).</span><span class="sxs-lookup"><span data-stu-id="f9d60-122">If you want to add a separator before or after the cascade menu item, use ECF\_SEPARATORBEFORE (0x20) or ECF\_SEPARATORAFTER (0x40).</span></span> <span data-ttu-id="f9d60-123">Eine Beschreibung dieser Flags von Windows 7 und höher finden Sie unter [**IExplorerCommand:: GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span><span class="sxs-lookup"><span data-stu-id="f9d60-123">For a description of these Windows 7 and later flags, see [**IExplorerCommand::GetFlags**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorercommand-getflags).</span></span> <span data-ttu-id="f9d60-124">ECF \_ separatorbefore funktioniert nur für Menü Elemente der obersten Ebene.</span><span class="sxs-lookup"><span data-stu-id="f9d60-124">ECF\_SEPARATORBEFORE works only for the top level menu items.</span></span> <span data-ttu-id="f9d60-125">MUIVerb ist vom Typ **reg \_ SZ**, und commandflags ist vom Typ **reg \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="f9d60-125">MUIVerb is of type **REG\_SZ**, and CommandFlags is of type **REG\_DWORD**.</span></span>

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

## <a name="remarks"></a><span data-ttu-id="f9d60-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9d60-126">Remarks</span></span>

<span data-ttu-id="f9d60-127">Der folgende Screenshot zeigt eine Abbildung der vorherigen Beispiele für den Registrierungsschlüssel Eintrag.</span><span class="sxs-lookup"><span data-stu-id="f9d60-127">The following screen shot is an illustration of the previous registry key entry examples.</span></span>

![Screenshot mit einem Beispiel für ein kaskadieres Menü, das die Auswahl von Editor und WordPad anzeigt](images/file-assoc/testcascademenu2.png)

 

 



