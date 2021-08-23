---
description: Die WMI-Klasse Win32 SerialPortConfiguration stellt die Einstellungen für die Datenübertragung an einem Windows \_ seriellen Anschluss dar. Dies schließt Konfigurationen zum Herstellen einer Verbindung und Fehlerüberprüfung ein.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Win32_SerialPortConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 07052c0366b32904ef6bf6f52b15f3ea98022ba8385120ec60cdefe5714e2c4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119079694"
---
# <a name="win32_serialportconfiguration-class"></a>Win32 \_ SerialPortConfiguration-Klasse

Die **WMI-Klasse \_ Win32 SerialPortConfiguration** stellt die Einstellungen für die Datenübertragung an einem Windows seriellen Anschluss dar. [](../wmisdk/retrieving-a-class.md) Dies schließt Konfigurationen zum Herstellen einer Verbindung und Fehlerüberprüfung ein.

Die folgende Syntax wurde aus MOF-Code (Managed Object Format, verwaltetes Objektformat) vereinfacht und enthält alle geerbten Eigenschaften. Eigenschaften werden in alphabetischer Reihenfolge und nicht in MOF-Reihenfolge aufgeführt.

## <a name="syntax"></a>Syntax

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a>Member

Die **Win32 \_ SerialPortConfiguration-Klasse** verfügt über die folgenden Membertypen:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **Win32 \_ SerialPortConfiguration-Klasse** verfügt über diese Eigenschaften.

<dl> <dt>

**AbortReadWriteOnError**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError")
</dt> </dl>

True **gibt an,** dass Lese- und Schreibvorgänge beendet werden, wenn ein Fehler auftritt. True **gibt an,** dass der Treiber alle Lese- und Schreibvorgänge mit einem Fehlerstatus beendet, wenn ein Fehler auftritt. Der Treiber akzeptiert keine weiteren Kommunikationsvorgänge, bis die Anwendung den Fehler bestätigt.

</dd> <dt>

**Baudrate**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| BaudRate")
</dt> </dl>

Baud-Rate (Bits pro Sekunde), mit der das Kommunikationsgerät betrieben wird.

Beispiel: 9600

</dd> <dt>

**BinaryModeEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")
</dt> </dl>

True **gibt an,** dass Datenübertragungen im binären Modus für den seriellen Anschluss aktiviert sind. Computersysteme, auf denen Windows, lassen nur binäre Übertragungen über serielle Anschlüsse zu, sodass dieser Wert immer **TRUE ist.**

</dd> <dt>

**BitsPerByte**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ByteSize")
</dt> </dl>

Anzahl der Bits, die für jedes Byte von Daten für den seriellen Windows gesendet und empfangen werden. Die Anzahl kann mit Steuerelement- und Fehlerkorrekturbits variieren, z. B. Paritätsbits.

Beispiel: 8

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Kurze Textbeschreibung des aktuellen Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**ContinueXMitOnXOff**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff")
</dt> </dl>

True **gibt** an, dass Datenübertragungen fortgesetzt werden, wenn der Eingabepuffer innerhalb von **XOffXMitThreshold-Bytes** liegt und der Treiber den **XOffChararcter-Wert** übertragen hat, um den Empfang von Bytes zu beenden. False **gibt** an, dass die Übertragung erst fortgesetzt wird, wenn sich der Eingabepuffer innerhalb von **XOnXMitThreshold-Bytes** befindet und der Treiber den **XOnCharacter-Wert** übertragen hat, um den Empfang wieder aufzunehmen.

</dd> <dt>

**CTSOutflowControl**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow")
</dt> </dl>

True **gibt an,** dass das CLEAR TO SEND-Signal (CTS) vor der Übertragung von Daten überprüft wird. CTS signalisiert, dass beide Geräte über die serielle Verbindung bereit sind, Daten zu übertragen. Die Datenübertragung wird angehalten, bis das CTS-Signal angegeben wird.

</dd> <dt>

**Beschreibung**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Textbeschreibung des aktuellen -Objekts.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**DiscardNULLBytes**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull")
</dt> </dl>

True **gibt an,** **dass NULL-Bytes** (Zeichen) verworfen werden, wenn sie empfangen werden.

</dd> <dt>

**DSROutflowControl**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow")
</dt> </dl>

True **gibt an,** dass die Datenflusssteuerung aktiviert ist, wenn eine DSR-Bedingung (Data Set Ready) vorgeschaltet ist. DSR signalisiert, dass die Verbindung von den Geräten über die serielle Verbindung hergestellt wurde. Die DSR-Datenübertragung wird angehalten, bis das DSR-Signal angegeben wird.

</dd> <dt>

**DSRSensitivity**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity")
</dt> </dl>

True **gibt an,** dass der Kommunikationstreiber den Zustand des DSR-Signals berücksichtigt. Der Treiber ignoriert alle empfangenen Bytes, es sei denn, die DSR-Modemeingabelinie ist hoch.

</dd> <dt>

**DTRFlowControlType**
</dt> <dd> <dl> <dt>

Datentyp: **string**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl")
</dt> </dl>

Verwendung der DTR-Flusssteuerung (Data Terminal Ready), nachdem eine Verbindung hergestellt wurde.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Aktivieren** ("Aktivieren")


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Deaktivieren** ("Deaktivieren")


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

**Handshake** ("Handshake")


</dt> <dd></dd> </dl>

</dd> <dt>

**EOFCharacter**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar")
</dt> </dl>

Der Wert des Zeichens, das zum Signalisieren des Datenendes verwendet wird.

Beispiel: ^Z

</dd> <dt>

**ErrorReplaceCharacter**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")
</dt> </dl>

Der Wert des Zeichens, das verwendet wird, um empfangene Bytes durch einen Paritätsfehler zu ersetzen.

Beispiel: ^C

</dd> <dt>

**ErrorReplacementEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar")
</dt> </dl>

True **gibt an,** dass bytes, die mit Paritätsfehlern empfangen werden, durch den **ErrorReplaceCharacter-Wert ersetzt** werden. Zeichen mit Paritätsfehlern werden nur ersetzt, wenn diese Eigenschaft **TRUE ist** und die Parität aktiviert ist.

</dd> <dt>

**EventCharacter**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar")
</dt> </dl>

Der Wert des Steuerzeichens, das verwendet wird, um ein Ereignis zu signalisieren, z. B. das Dateiende.

Beispiel: ^e

</dd> <dt>

**Isbusy**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| File Functions \| CreateFile")
</dt> </dl>

True **gibt an,** dass der serielle Anschluss ausgelastet ist.

</dd> <dt>

**Name**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**Schlüssel,**](../wmisdk/key-qualifier.md) [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SerialComm")
</dt> </dl>

Name des Windows seriellen Anschlusses.

Beispiel: "COM1"

</dd> <dt>

**Parität**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| Parity")
</dt> </dl>

Methode der zu verwendenden Paritätsüberprüfung. Parität wird als Fehlerüberprüfungstechnik verwendet, bei der in jeder Dateneinheit ein zusätzliches Paritätsbit enthalten ist. Der Empfänger kann dann die Gültigkeit der Daten überprüfen, indem er die festgelegten Bits zählt.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")


</dt> <dd>

Paritätsprüfung wird nicht verwendet.

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Ungerade** ("ungerade")


</dt> <dd>

Legt das Paritätsbit fest, sodass die Anzahl der festgelegten Bits eine ungerade Zahl ist.

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Even** ("Even")


</dt> <dd>

Legt das Paritätsbit fest, sodass die Anzahl der festgelegten Bits eine gerade Zahl ist.

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")


</dt> <dd>

Behält die Festlegung des Paritätsbits auf 1 bei.

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Leerzeichen** ("Leerzeichen")


</dt> <dd>

Belässt das Paritätsbit auf 0 (null).

</dd> </dl>

</dd> <dt>

**ParityCheckEnabled**
</dt> <dd> <dl> <dt>

Datentyp: **boolescher Wert**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity")
</dt> </dl>

True **gibt an,** dass die Paritätsprüfung aktiviert ist.

</dd> <dt>

**RTSFlowControlType**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> </dl>

Anforderung zum Senden (RTS)-Flusssteuerung. RTS wird verwendet, um zu signalisieren, dass Daten für die Übertragung verfügbar sind.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Aktivieren** ("Aktivieren")


</dt> <dd>

RTS bleibt für die Datenübertragungssitzung übrig.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deaktivieren** ("Deaktivieren")


</dt> <dd>

RTS wird ignoriert, nachdem das erste RTS-Signal empfangen wurde.

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Handshake** ("Handshake")


</dt> <dd>

RTS wird deaktiviert, wenn der Übertragungspuffer mehr als drei Viertel voll ist, und RTS wird aktiviert, wenn der Puffer weniger als eine Hälfte voll ist.

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Umschalten** ("Umschalten")


</dt> <dd>

RTS wird aktiviert, wenn Daten für die Übertragung gepuffert werden.

</dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Bezeichner, unter dem das aktuelle Objekt bekannt ist.

Diese Eigenschaft wird von der [**CIM-Einstellung \_ geerbt.**](cim-setting.md)

</dd> <dt>

**Stoppbits**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| StopBits")
</dt> </dl>

Anzahl der zu verwendenden Stoppbits. Stoppbits trennen jede Dateneinheit in einer asynchronen seriellen Verbindung. Sie werden auch fortlaufend gesendet, wenn keine Daten für die Übertragung verfügbar sind.

<dt>

<span id="1"></span>

**1** ("1")


</dt> <dd></dd> <dt>

<span id="1.5"></span>

**1.5** ("1.5")


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** ("2")


</dt> <dd></dd> </dl>

</dd> <dt>

**XOffCharacter**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")
</dt> </dl>

Der Wert des XOFF-Zeichens für die Übertragung und den Empfang. XOFF ist ein Softwaresteuerelemente zum Beenden der Datenübertragung (während RTS und CTS Hardwaresteuerelemente sind). XON setzt die Übertragung wieder ein.

</dd> <dt>

**XOffXMitThreshold**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim")
</dt> </dl>

Maximale Anzahl von Bytes, die im Eingabepuffer zulässig sind, bevor das XOFF-Zeichen gesendet wird.

</dd> <dt>

**XOnCharacter**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")
</dt> </dl>

Der Wert des XON-Zeichens für Übertragung und Empfang. XON ist eine Softwaresteuerung zum Fortsetzen der Datenübertragung (während RTS und CTS Hardwarekontrollen sind). XOFF beendet die Übertragung.

</dd> <dt>

**XOnXMitThreshold**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")
</dt> </dl>

Mindestanzahl von Bytes, die im Eingabepuffer zulässig sind, bevor das XON-Zeichen gesendet wird. Diese Eigenschaft arbeitet mit **XOffXMitThreshold** zusammen, um die Rate zu steuern, mit der Daten übertragen werden.

</dd> <dt>

**XOnXOffInFlowControl**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX")
</dt> </dl>

True gibt an, dass während des Empfangs die Flusssteuerung STOCK/XOFF verwendet wird. **TRUE** gibt an, dass der **XOffCharacter-Wert** gesendet wird, wenn der Eingabepuffer innerhalb von **XOffXMitThreshold** Bytes von full und der **XOnCharacter-Wert** gesendet wird, wenn der Eingabepuffer innerhalb von **XOnXMitThreshold** Bytes von leer ist.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

FALSE

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

TRUE

</dd> </dl>

</dd> <dt>

**XOnXOffOutFlowControl**
</dt> <dd> <dl> <dt>

Datentyp: **uint32**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX")
</dt> </dl>

**XOnXOffOutFlowControl** gibt an, ob während der Übertragung die Flusssteuerung TEXAS oder XOFF verwendet wird. True gibt an, dass die Übertragung beendet wird, wenn der **XOffCharacter-Wert** empfangen wird, und erneut gestartet wird, wenn der **XOnCharacter-Wert** empfangen wird.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Die **Win32 \_ SerialPortConfiguration-Klasse** wird von [**der \_ CIM-Einstellung**](cim-setting.md)abgeleitet.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Vista<br/>                                                                |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2008<br/>                                                          |
| Namespace<br/>                | \\Stamm-CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_CIM-Einstellung**](cim-setting.md)
</dt> <dt>

[Computersystemhardwareklassen](computer-system-hardware-classes.md)
</dt> </dl>

 

 
