---
description: Der Installer legt die Patch-Eigenschaft auf eine Liste der angewendeten Patches fest, indem msiapplypatch, msiapplymultiplepatches oder die Befehlszeilen Option/p aufgerufen wird.
ms.assetid: f2993544-2124-4fb0-8bb3-59f5d8e76b83
title: Patch-Eigenschaft
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e870c480c1fdff0f979701e059bfcd6eb187a4a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106358685"
---
# <a name="patch-property"></a>Patch-Eigenschaft

Der Installer legt die **Patch** -Eigenschaft auf eine Liste der angewendeten Patches fest, indem [**msiapplypatch**](/windows/desktop/api/Msi/nf-msi-msiapplypatcha), [**msiapplymultiplepatches**](/windows/desktop/api/Msi/nf-msi-msiapplymultiplepatchesa) oder die [Befehlszeilen Option](command-line-options.md)/p aufgerufen wird. Sie können die **Patch** -Eigenschaft auch in der Befehlszeile festlegen, wenn Sie ein Paket mit [**msiinstallproduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) oder der/i-Befehlszeilen Option installieren.

Der Wert der **Patch** -Eigenschaft ist eine Liste der Patches, die installiert werden. Jeder Patch in der Liste wird durch den vollständigen Pfad zum Paket des Patches (MSP-Datei) repräsentiert. Die vollständigen Pfade in der Liste werden durch Semikolons getrennt.

**Windows Installer 2,0:** Mehrere Patches werden nicht unterstützt. Windows Installer 3,0 ist zum Anwenden mehrerer Patches erforderlich.

## <a name="remarks"></a>Bemerkungen

Wenn Sie mit [Msimsp.exe](msimsp-exe.md) ein Patchpaket erstellen und [Patchwiz.dll](patchwiz-dll.md) können Sie angeben, dass eine Aktion oder ein Dialogfeld nur ausgeführt wird, wenn ein bestimmter Patch angewendet wird. Wenn Sie das Patchpaket erstellen, z. b. "Test. msp", erstellen Sie ein aktualisiertes Image des Produkts und eine Eigenschaften Datei für die Patcherstellung. Wenn Sie die Eigenschaften Datei für die Patcherstellung erstellen, können Sie einen Eigenschaftsnamen (z. b. patchfortest) in das Feld "mediasrcpropname" der Tabelle " [ImageFamilies](imagefamilies-table-patchwiz-dll-.md) " eingeben. Wenn Sie die Sequenz Tabellen des aktualisierten Abbilds des Produkts erstellen, können Sie in die Spalte Bedingung der Sequenz Tabelle eine Bedingungs Anweisung für die Aktion oder das Dialogfeld einschließen, die Sie bedingen möchten.

Beispielsweise können Sie die folgende Bedingungs Anweisung verwenden, um eine Aktion oder ein Dialogfeld nur dann auszuführen, wenn "Test. msp" angewendet wird.

<dl> Patch und patchfortest und Patch >< patchfortest  
</dl>

> [!Note]  
> Da die **patcheigenschaft** mehrere Patches enthalten kann, verwenden Sie den Teil Zeichenfolge-Operator "><", um zu prüfen, ob ein bestimmter Patch statt der Gleichheits Operator "=" vorhanden ist. Weitere Informationen zu bedingten Anweisungen finden Sie im Abschnitt [Syntax der Bedingungs Anweisung](conditional-statement-syntax.md) .

 

Der Installer legt beide Eigenschaften fest, wenn Sie eine Liste von Patches, die "Test. msp" enthalten, anwenden. Beispielsweise können Sie die [Befehlszeilen Option](command-line-options.md) /p verwenden, um eine Liste mit zwei Patches anzuwenden.

**msiexec/qb/p \\ \\ Scratch \\ , Scratch- \\ \\ Patches \\ , Test. msp; \\ \\ Scratch \\ - \\ \\ Balken. msp Scratch**

Der Installer legt die **Patch** -und patchfortest-Eigenschaften wie folgt fest.

<dl> Patch = Scratch Scratch- \\ \\ \\ Patches ( \\ \\ \\ Test. msp \\ \\ ) Scratch \\ - \\ \\ Balken. msp Scratch  
Patchfortest = Scratch Scratch- \\ \\ \\ Patches- \\ \\ \\ Test. msp  
</dl>

In diesem Fall ist die Bedingung "true", und die oben beschriebene bedingte Aktion oder das obige Dialogfeld kann für jeden installierten Patch ausgeführt werden: "Test. msp" und "Bar. msp".

Wenn "Test. msp" nicht angewendet wird, schließt das Installationsprogramm es nicht in die **patcheigenschaft** ein und legt "patchfortest" nicht fest. In diesem Fall ist die oben genannte Bedingung false, und die bedingte Aktion oder das Dialogfeld wird nicht ausgeführt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 unter Windows Server 2012, Windows 8, Windows Server 2008 R2 oder Windows 7. Windows Installer 4,0 oder Windows Installer 4,5 unter Windows Server 2008 oder Windows Vista. Windows Installer unter Windows Server 2003 oder Windows XP. Informationen zu den minimalen Windows-Service Pack, die für eine Windows Installer Version erforderlich sind, finden Sie in den [Windows Installer Run-Time Anforderungen](windows-installer-portal.md) .<br/> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Eigenschaften](properties.md)
</dt> <dt>

[Syntax der bedingten Anweisung](conditional-statement-syntax.md)
</dt> <dt>

[Beispiele für bedingte Anweisungs Syntax](examples-of-conditional-statement-syntax.md)
</dt> </dl>

 

 




