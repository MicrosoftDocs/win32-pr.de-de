---
description: Standardmäßig empfängt eine Anwendung oder ein Skript Daten vom entsprechenden Anbieter, wenn zwei Versionen von Anbietern vorhanden sind.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Anfordern von WMI-Daten auf einer 64-Bit-Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fd392d482f083a3c1b1dff3b90d70f1857aeebb4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356877"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a>Anfordern von WMI-Daten auf einer 64-Bit-Plattform

Standardmäßig empfängt eine Anwendung oder ein Skript Daten vom entsprechenden Anbieter, wenn zwei Versionen von Anbietern vorhanden sind. Der 32-Bit-Anbieter gibt Daten an eine 32-Bit-Anwendung zurück, einschließlich aller Skripts, und der 64-Bit-Anbieter gibt Daten an die von 64 Bit kompilierten Anwendungen zurück. Allerdings kann eine Anwendung oder ein Skript Daten vom nicht standardmäßigen Anbieter anfordern, wenn dies der Fall ist, indem WMI über Flags für Methodenaufrufe benachrichtigt wird.

## <a name="context-flags"></a>Kontextflags

Die zeichenfolgenflags **\_ \_ providerarchitecture** und Requirements **\_ \_ darchitecture** verfügen über eine Reihe von Werten, die von WMI verarbeitet, jedoch nicht in SDK-Header-oder Typbibliotheks Dateien definiert sind. Die Werte werden in einen Kontext Parameter eingefügt, um WMI zu signalisieren, dass Daten vom nicht standardmäßigen Anbieter angefordert werden sollen.

Im folgenden werden die Flags und die möglichen Werte aufgeführt.

<dl> <dt>

<span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_Providerarchitecture**
</dt> <dd>

Ganzzahliger Wert, entweder 32 oder 64, der die 32-Bit-oder 64-Bit-Version angibt.

</dd> <dt>

<span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_Requirements darchitecture**
</dt> <dd>

Boolescher Wert, der zusätzlich zu **\_ \_ providerarchitecture** verwendet wird, um das Laden der angegebenen Anbieter Version zu erzwingen. Wenn die Version nicht verfügbar ist, gibt WMI den Fehler 0x80041013, **wbemErrProviderLoadFailure** für die Visual Basic und den **\_ \_ \_ Lade \_ Fehler des WBEM E-Anbieters** für C++ zurück. Der Standardwert für dieses Flag, wenn es nicht angegeben ist, ist **false**.

</dd> </dl>

Auf einem 64-Bit-System, das über parallele Versionen eines Anbieters verfügt, empfängt eine 32-Bit-Anwendung oder ein-Skript automatisch Daten vom 32-Bit-Anbieter, es sei denn, diese Flags werden bereitgestellt und geben an, dass die 64-Bit-Anbieter Daten zurückgegeben werden sollen.

## <a name="using-the-context-flags"></a>Verwenden der kontextflags

C++-Anwendungen können die [**IWbemContext**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) -Schnittstelle mit [**IWbemServices:: ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) verwenden, um die Verwendung eines nicht standardmäßigen Anbieters mit WMI zu kommunizieren.

Bei der Skripterstellung und Visual Basic müssen Sie ein Objekt vom Typ "WS- [**namedvalueset**](swbemnamedvalueset.md) " erstellen, das die Flags für den *objwbemnamedvalueset* -Parameter von [**SWbemServices.Execmethod**](swbemservices-execmethod.md)enthält. Weitere Informationen zum Einrichten der Parameter Objekte für diesen Befehl finden Sie unter [Erstellen von inparameter-Objekten und Auswerten von outparameter-Objekten](constructing-inparameters-objects-and-parsing-outparameters-objects.md).

Sie können Skripts und Anwendungen auf sichere Weise mithilfe der kontextflags in älteren Betriebssystemen ausführen, da Sie von WMI in Systemen ignoriert werden, in denen Sie nicht implementiert sind. Während 32-Bit-und 64-Bit-Versionen des System Registrierungs Anbieters vorhanden sind, beachten Sie, dass nur eine Version des WMI-Repository vorhanden ist.

## <a name="accessing-the-default-registry-hive"></a>Zugreifen auf die standardmäßige Registrierungs Struktur

In der folgenden Reihe von Beispielen wird der [Registrierungs Anbieter](/previous-versions/windows/desktop/regprov/system-registry-provider)verwendet, bei dem auf 64-Bit-Betriebssystemen nebeneinander 32-Bit-und 64-Bit-Versionen vorinstalliert sind. In diesen Beispielen erhalten 32-Bit-Clients vom Anbieter zurückgegebene Daten vom 32-Bit-Knoten **HKEY \_ local \_ Machine \\ Software \\ Wow6432Node \\ Microsoft**. 64-Bit-Clients erhalten vom Anbieter zurückgegebene Daten vom 64-Bit-Knoten **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Logging**.

Die Skripts veranschaulichen, wie Sie die Methoden der Klasse [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov) der Registrierung über [**SWbemServices.Execmethod**](swbemservices-execmethod.md) zum Abrufen von Daten aus der 32-Bit-Registrierungs Struktur abrufen.

Das folgende Skript ruft Daten vom Anbieter ab, die mit der Bitbreite des Aufrufers übereinstimmen (in diesem Fall 64 Bits), da es sich um ein Skript handelt, das unter dem 64-Bit Windows Script Host (WSH) ausgeführt wird. Das Skript ruft den Wert aus dem 64-Bit-Registrierungs Knoten **HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ WBEM \\ CIMOM \\ Logging** anstelle des 32-Bit-Knotens **HKEY \_ local \_ Machine \\ Software \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM** ab.


```VB
strComputer = "."
Const HKLM = &h80000002
Set objReg = Getobject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" & strComputer _
    & "\root\default:stdregprov")
'Set up inParameters object
Set Inparams = objReg.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objReg.ExecMethod_("GetStringValue", Inparams)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



Wenn der **Protokollierungs** Wert in der standardhive auf 1 festgelegt ist, sollte die Ausgabe des Skripts in etwa wie folgt aussehen:

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Beispiel: Anfordern der 32-Bit-Registrierungs Struktur auf einem 64-Bit-Computer

Im folgenden geänderten Beispiel des Standard Skripts wird das Flag für die **\_ \_ providerarchitecture** -Zeichenfolge verwendet, um Zugriff auf die 32-Bit-Registrierungsdaten auf einem 64-Bit-Computer anzufordern. Der Aufrufer ist mit der 32-Bit-Struktur verbunden, unabhängig davon, ob es sich um eine 32-oder 64-Bit-Anwendung handelt.


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Beispiel: Erzwingen von WMI für den Zugriff auf die 32-Bit-Registrierungs Struktur auf einem 64-Bit-Computer

Durch die folgende Änderung des obigen Skripts durch Hinzufügen der Flags **\_ \_ providerarchitecture** und Requirements **\_ \_ darchitecture** zum Kontext Parameter wird WMI gezwungen, den 32-Bit-Anbieter zu laden und 32-Bit-Daten zu erhalten. Wenn der Anbieter nicht vorhanden ist, tritt ein Fehler beim Laden des Anbieters auf. Das Kontext Objekt muss bei der Verbindung mit WMI durch Aufrufen von "WS- [**Locator. ConnectServer**](swbemlocator-connectserver.md)" bereitgestellt werden.


```VB
strComputer = "."
Const HKLM = &h80000002
Set objCtx = CreateObject("WbemScripting.SWbemNamedValueSet")
objCtx.Add "__ProviderArchitecture", 32
objCtx.Add "__RequiredArchitecture", TRUE
Set objLocator = CreateObject("Wbemscripting.SWbemLocator")
Set objServices = objLocator.ConnectServer(strComputer,"root\default","","",,,,objCtx)
Set objStdRegProv = objServices.Get("StdRegProv") 

' Use ExecMethod to call the GetStringValue method
Set Inparams = objStdRegProv.Methods_("GetStringValue").Inparameters
Inparams.Hdefkey = HKLM
Inparams.Ssubkeyname = "Software\Microsoft\Wbem\CIMOM"
Inparams.Svaluename = "Logging"
set Outparams = objStdRegProv.ExecMethod_("GetStringValue", Inparams,,objCtx)

'Show output parameters object and the registry value HKLM\SOFTWARE\
WScript.Echo Outparams.GetObjectText_
WScript.Echo "WMI Logging is set to  " & Outparams.SValue
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erhalten und Bereitstellen von Daten auf einem 64-Bit-Computer](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
