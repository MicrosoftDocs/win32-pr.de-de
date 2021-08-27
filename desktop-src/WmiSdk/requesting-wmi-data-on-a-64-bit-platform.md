---
description: Standardmäßig empfängt eine Anwendung oder ein Skript Daten vom entsprechenden Anbieter, wenn zwei Versionen von Anbietern vorhanden sind.
ms.assetid: 379d934e-e010-4a03-8dc1-121be43e4c6f
ms.tgt_platform: multiple
title: Anfordern von WMI-Daten auf einer 64-Bit-Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 320aaec9f11600e3b963a01fe9dcddbd6c4f1f3fd98df8ff2311417ddcd6fef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119995780"
---
# <a name="requesting-wmi-data-on-a-64-bit-platform"></a>Anfordern von WMI-Daten auf einer 64-Bit-Plattform

Standardmäßig empfängt eine Anwendung oder ein Skript Daten vom entsprechenden Anbieter, wenn zwei Versionen von Anbietern vorhanden sind. Der 32-Bit-Anbieter gibt Daten an eine 32-Bit-Anwendung zurück, einschließlich aller Skripts, und der 64-Bit-Anbieter gibt Daten an die kompilierten 64-Bit-Anwendungen zurück. Eine Anwendung oder ein Skript kann jedoch Daten vom Nichtstandardanbieter anfordern, sofern vorhanden, indem WMI über Flags bei Methodenaufrufen benachrichtigt wird.

## <a name="context-flags"></a>Kontextflags

Die Zeichenfolgenflags **\_ \_ ProviderArchitecture** und **\_ \_ RequiredArchitecture** verfügen über einen Satz von Werten, die von WMI verarbeitet, aber nicht in SDK-Header- oder Typbibliotheksdateien definiert sind. Die Werte werden in einem Kontextparameter platziert, um WMI zu signalisieren, dass Daten vom Nichtstandardanbieter angefordert werden sollen.

Im Folgenden werden die Flags und ihre möglichen Werte aufgelistet.

<dl> <dt>

<span id="__ProviderArchitecture"></span><span id="__providerarchitecture"></span><span id="__PROVIDERARCHITECTURE"></span>**\_\_ProviderArchitecture**
</dt> <dd>

Ganzzahliger Wert ( 32 oder 64), der die 32-Bit- oder 64-Bit-Version angibt.

</dd> <dt>

<span id="__RequiredArchitecture"></span><span id="__requiredarchitecture"></span><span id="__REQUIREDARCHITECTURE"></span>**\_\_RequiredArchitecture**
</dt> <dd>

Boolescher Wert, der zusätzlich zu **\_ \_ ProviderArchitecture** verwendet wird, um das Laden der angegebenen Anbieterversion zu erzwingen. Wenn die Version nicht verfügbar ist, gibt WMI den Fehler 0x80041013, **wbemErrProviderLoadFailure** für Visual Basic und **WBEM \_ E PROVIDER LOAD \_ \_ \_ FAILURE** für C++ zurück. Der Standardwert für dieses Flag, wenn es nicht angegeben ist, ist **FALSE.**

</dd> </dl>

Auf einem 64-Bit-System mit nebeneinander ausgeführten Versionen eines Anbieters empfängt eine 32-Bit-Anwendung oder ein 32-Bit-Skript automatisch Daten vom 32-Bit-Anbieter, es sei denn, diese Flags werden bereitgestellt und geben an, dass die 64-Bit-Anbieterdaten zurückgegeben werden sollen.

## <a name="using-the-context-flags"></a>Verwenden der Kontextflags

C++-Anwendungen können die [**IWbemContext-Schnittstelle**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemcontext) mit [**IWbemServices::ExecMethod**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execmethod) verwenden, um die Verwendung eines Nichtstandardanbieters an WMI zu kommunizieren.

In Skripts und Visual Basic müssen Sie ein [**SWbemNamedValueSet-Objekt**](swbemnamedvalueset.md) erstellen, das die Flags für den *objWbemNamedValueSet-Parameter* von [**SWbemServices.ExecMethod**](swbemservices-execmethod.md)enthält. Weitere Informationen zum Einrichten der Parameterobjekte für diesen Aufruf finden Sie unter [Erstellen von InParameters-Objekten und Analysieren von OutParameters-Objekten.](constructing-inparameters-objects-and-parsing-outparameters-objects.md)

Sie können Skripts und Anwendungen sicher mithilfe der Kontextflags in älteren Betriebssystemen ausführen, da WMI sie in Systemen ignoriert, in denen sie nicht implementiert sind. Obwohl 32-Bit- und 64-Bit-Versionen des Systemregistrierungsanbieters vorhanden sind, beachten Sie, dass nur eine Version des WMI-Repositorys vorhanden ist.

## <a name="accessing-the-default-registry-hive"></a>Zugreifen auf die Standardregistrierungsstruktur

In der folgenden Reihe von Beispielen wird der [Registrierungsanbieter](/previous-versions/windows/desktop/regprov/system-registry-provider)verwendet, bei dem 32-Bit- und 64-Bit-Versionen auf 64-Bit-Betriebssystemen vorinstalliert sind. In diesen Beispielen erhalten 32-Bit-Clients Daten, die vom Anbieter vom 32-Bit-Knoten **HKEY \_ LOCAL MACHINE SOFTWARE \_ \\ \\ Wow6432Node \\ Microsoft** zurückgegeben werden. 64-Bit-Clients erhalten Daten, die vom Anbieter vom 64-Bit-Knoten HKEY LOCAL MACHINE SOFTWARE Microsoft Logging zurückgegeben **\_ \_ \\ \\ \\ werden.**

Die Skripts zeigen, wie die Methoden der Registry [**StdRegProv-Klasse**](/previous-versions/windows/desktop/regprov/stdregprov) über [**SWbemServices.ExecMethod**](swbemservices-execmethod.md) aufgerufen werden, um Daten aus der 32-Bit-Registrierungsstruktur abzurufen.

Das folgende Skript ruft Daten vom Anbieter ab, der der Bitbreite des Aufrufers entspricht (in diesem Fall 64 Bits), da es sich um ein Skript handelt, das unter dem 64-Bit-Windows Script Host (WSH) ausgeführt wird. Das Skript ruft den Wert vom 64-Bit-Registrierungsknoten **HKEY \_ LOCAL MACHINE SOFTWARE Microsoft \_ \\ \\ \\ WBEM \\ CIMOM \\ Logging** anstelle des 32-Bit-Knotens **HKEY LOCAL MACHINE SOFTWARE \_ \_ \\ \\ Wow6432Node \\ Microsoft \\ WBEM \\ CIMOM** ab.


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



Wenn der **Protokollierungswert** in der Standardstruktur auf 1 festgelegt ist, sollte die Ausgabe des Skripts in etwa wie folgt aussehen:

``` syntax
instance of __PARAMETERS
{
    ReturnValue = 0;
    sValue = "1";
};
WMI Logging is set to 1
```

## <a name="example-specifically-requesting-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Beispiel: Explizites Anfordern der 32-Bit-Registrierungsstruktur auf einem 64-Bit-Computer

Im folgenden geänderten Beispiel des Standardskripts wird das Zeichenfolgenflag **\_ \_ ProviderArchitecture** verwendet, um Zugriff auf die 32-Bit-Registrierungsdaten auf einem 64-Bit-Computer anzufordern. Der Aufrufer ist mit der 32-Bit-Struktur verbunden, unabhängig davon, ob es sich um eine 32- oder 64-Bit-Anwendung handelt.


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



## <a name="example-forcing-wmi-to-access-the-32-bit-registry-hive-on-a-64-bit-computer"></a>Beispiel: Erzwingen von WMI für den Zugriff auf die 32-Bit-Registrierungsstruktur auf einem 64-Bit-Computer

Die folgende Änderung des obigen Skripts durch Hinzufügen der **\_ \_ Flags ProviderArchitecture** und **\_ \_ RequiredArchitecture** zum Kontextparameter zwingt WMI, den 32-Bit-Anbieter zu laden und 32-Bit-Daten abzurufen. Wenn der Anbieter nicht vorhanden ist, tritt ein Anbieterladefehler auf. Das Kontextobjekt muss in der Verbindung mit WMI durch Aufrufen von [**SWbemLocator.ConnectServer**](swbemlocator-connectserver.md)angegeben werden.


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

[Abrufen und Bereitstellen von Daten auf einem 64-Bit-Computer](getting-and-providing-data-on-a-64-bit-computer.md)
</dt> </dl>

 

 
